React tutorial - TicTacToe


step 1
    npm create vite@latest . -- --template react

step 2
    follow steps from https://react.dev/learn/tutorial-tic-tac-toe

to deploy in github.io
    source: https://www.youtube.com/watch?v=hn1IkJk24ow
    reference: https://github.com/gitname/react-gh-pages

    Install gh-pages as a dependency
        npm install gh-pages --save-dev

    deploy to subdir in github.io
    Settings -> Pages
        Source: Deploy from a branch
        Branch: gh-pages 
    Location is defined in file: package.json, under "homepage" ie
        "homepage" : "https://bbttko.github.io/react_ttt/",
    other package.json changes:
        under scripts:
            "predeploy" : "npm run build",
            "deploy" : "gh-pages -d build",
    git add .
    git commit -m "commit msg"
    git push origin main
    npm run deploy


