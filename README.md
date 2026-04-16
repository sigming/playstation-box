<p align="center">
  <a href="https://gist.github.com/Swilder-M/441f57c231581fca04fb569fda82ec91"><img width="400" src="https://raw.githubusercontent.com/Swilder-M/playstation-box/master/assets/pinned.png"></a>
  <h3 align="center">🎮 playstation-box</h3>
  <p align="center">Update a pinned gist to contain your PlayStation stats</p>
</p>

## Setup
1. Fork [this repository](https://github.com/Swilder-M/playstation-box).

2. Create a new public GitHub Gist at <https://gist.github.com/>.

3. Create a new token at <https://github.com/settings/personal-access-tokens/new> with the following settings:
   - Expiration: Select Custom and set it to 1 year. (Note: You will need to renew the token annually.)
   - Repository access: Select `Only select repositories` and choose your forked repository.
   - Repository permissions: Enable `Secrets` with read and write access, and `Metadata` with read-only access.
   - Account permissions: Enable `Gists` with read and write access.
   - See the [complete setup reference](https://github.com/Swilder-M/playstation-box/blob/master/assets/github-token.png) for details.

4. Sign in to the PlayStation Store at <https://library.playstation.com/recently-purchased>.

5. Open the following link: <https://ca.account.sony.com/api/v1/ssocookie>, and copy the `npsso` value.

6. Go to your repository's **Settings > Secrets** and add the following environment variables:
   - PSN_NPSSO: The `npsso` value you copied in step 5.
   - GH_TOKEN: The token you created in step 3.
   - GIST_ID: The ID portion of your gist URL: `https://gist.github.com/your_name/<GIST_ID>`.
