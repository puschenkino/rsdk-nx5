apt install npm jq jsonnet
git clone --recurse-submodules https://github.com/RadxaOS-SDK/rsdk.git
wget  https://raw.githubusercontent.com/puschenkino/rsdk-nx5/refs/heads/main/products.json -O /root/rsdk/src/share/rsdk/configs/products.json
cd rsdk
npm install @devcontainers/cli
export PATH="$PWD/src/bin:$PWD/node_modules/.bin:$PATH"
rsdk devcon up
rsdk devcon
rsdk build rock-5b-plus bookworm cli
