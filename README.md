# git-secure-sign

### A more secure way to sign your commits

git-secure-sign allows for sigining Git commits on a separate computer from the
one you created the commit with. This prevents your PGP private key from ever
leaving the safety of your signing computer since all the signing is done there.

### How to Use
1. Prepare the commit you want to make with `git add`
2. Run `git secure-sign --store <source> <destination>`. The `source` should be
   the Git repository you want to make the commit in, and the `destination`
   should where you want to store it (like a flash drive).
3. Put the flash drive into your signing computer.
4. Run `git secure-sign --sign <stored location>` to sign the commit on your
   flash drive from your signing computer.
5. Put the flash drive back into your main computer.
6. Run `git secure-sign --commit <git repo> <stored location>` to add the signed
   commit to your Git repository.
