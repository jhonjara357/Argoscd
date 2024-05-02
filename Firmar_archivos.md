certificado prueba1
gpg --full-generate-key
gpg --list-secret-keys --keyid-format=long

git config --global user.email xxxxxx@gmail.com
git config --global user.name xxxyyyzzz

git config --global user.signingkey 0AF19XXXX8601AAE
git config --global commit.pgpsign true
git log --show-signature -1


gpg --armor --export 0AF19XXXX8601AAE 
gpg --export --armor 0AF19XXXX8601AAE > ./gpg-key.pub
gpg --export-secret-keys --armor 2F2E4E774B8FDEDFCEF149890AF19XXXX8601AAE > ./gpg-key.asc


gpg --delete-keys 0AF19XXXX8601AAE
gpg --delete-secret-keys 0AF19XXXX8601AAE

gpg --edit-key 0AF19XXXX8601AAE 