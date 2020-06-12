# Testing

## Link module
    npm link

## Link module from another project
    npm link <package.json.name>

# npm

## Login / Logout

    npm login
    npm logout
    
## Profile
    
    npm profile get
    npm whoami

## Publishing

First Publish:

    npm publish --access public
    
Subsequent Publishes:

    npm publish

Publish only specific tag:

    npm publish --tag develop
    
## Unpublishing

    npm unpublish <package-name> -f
    npm unpublish <package-name>@<version>

# Automated CI

1) Get your API Token from NPM
  - Settings > Auth Token > Create New Token > Read & Publish
  - Copy the token

2) Add this API as as secret to your GitHub repo
  - Settings > Secrets > New secret
  - Name: NPM_TOKEN
  - Value: <paste the token from step 1>

## Publishing by pushing to branch

**npm/next**
- Pushing to npm/next branch will publish a new package with the 'next' tag
- Version name will be x.x.x-next.<build-no>

**master**
- Pushing to master will publish a new package with the 'latest' tag
- Version name will be x.x.x

*x.x.x is obtained from package.json.version 
