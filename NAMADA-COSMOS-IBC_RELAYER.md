# NAMADA-COSMOS-IBC-RELAYER #

### Proof Of Create Chanel Namada - Cosmos
```
root@vmi1682379:~# export HERMES_CONFIG=$HOME/.hermes/config.toml
root@vmi1682379:~# hermes --config $HERMES_CONFIG \
  create channel \
  --a-chain shielded-expedition.88f17d1d14 \
  --b-chain theta-testnet-001 \
  --a-port transfer \
  --b-port transfer \
  --new-client-connection --yes
2024-03-24T03:57:45.625636Z  INFO ThreadId(01) running Hermes v1.7.4+38f41c6
2024-03-24T03:57:46.199261Z  INFO ThreadId(01) Creating new clients, new connection, and a new channel with order ORDER_UNORDERED
2024-03-24T03:58:14.644398Z  INFO ThreadId(01) foreign_client.create{client=theta-testnet-001->shielded-expedition.88f17d1d14:07-tendermint-0}: 🍭 client was created successfully id=07-tendermint-3257
2024-03-24T03:58:18.862096Z  INFO ThreadId(01) foreign_client.create{client=shielded-expedition.88f17d1d14->theta-testnet-001:07-tendermint-0}: 🍭 client was created successfully id=07-tendermint-3479
2024-03-24T03:58:45.656345Z  INFO ThreadId(01) 🥂 shielded-expedition.88f17d1d14 => OpenInitConnection(OpenInit { Attributes { connection_id: connection-1623, client_id: 07-tendermint-3257, counterparty_connection_id: None, counterparty_client_id: 07-tendermint-3479 } }) at height 0-210918
2024-03-24T03:59:32.765018Z  INFO ThreadId(01) 🥂 theta-testnet-001 => OpenTryConnection(OpenTry { Attributes { connection_id: connection-3594, client_id: 07-tendermint-3479, counterparty_connection_id: connection-1623, counterparty_client_id: 07-tendermint-3257 } }) at height 0-20881315
2024-03-24T04:00:09.037953Z  INFO ThreadId(01) 🥂 shielded-expedition.88f17d1d14 => OpenAckConnection(OpenAck { Attributes { connection_id: connection-1623, client_id: 07-tendermint-3257, counterparty_connection_id: connection-3594, counterparty_client_id: 07-tendermint-3479 } }) at height 0-210925
2024-03-24T04:00:26.202616Z  INFO ThreadId(01) 🥂 theta-testnet-001 => OpenConfirmConnection(OpenConfirm { Attributes { connection_id: connection-3594, client_id: 07-tendermint-3479, counterparty_connection_id: connection-1623, counterparty_client_id: 07-tendermint-3257 } }) at height 0-20881324
2024-03-24T04:00:29.506611Z  INFO ThreadId(01) connection handshake already finished for Connection { delay_period: 0ns, a_side: ConnectionSide { chain: BaseChainHandle { chain_id: shielded-expedition.88f17d1d14 }, client_id: 07-tendermint-3257, connection_id: connection-1623 }, b_side: ConnectionSide { chain: BaseChainHandle { chain_id: theta-testnet-001 }, client_id: 07-tendermint-3479, connection_id: connection-3594 } }
2024-03-24T04:00:49.120459Z  INFO ThreadId(01) 🎊  shielded-expedition.88f17d1d14 => OpenInitChannel(OpenInit { port_id: transfer, channel_id: channel-1051, connection_id: None, counterparty_port_id: transfer, counterparty_channel_id: None }) at height 0-210929
2024-03-24T04:01:04.054434Z  INFO ThreadId(01) 🎊  theta-testnet-001 => OpenTryChannel(OpenTry { port_id: transfer, channel_id: channel-4088, connection_id: connection-3594, counterparty_port_id: transfer, counterparty_channel_id: channel-1051 }) at height 0-20881331
2024-03-24T04:01:38.987783Z  INFO ThreadId(01) 🎊  shielded-expedition.88f17d1d14 => OpenAckChannel(OpenAck { port_id: transfer, channel_id: channel-1051, connection_id: connection-1623, counterparty_port_id: transfer, counterparty_channel_id: channel-4088 }) at height 0-210934
2024-03-24T04:01:54.754467Z  INFO ThreadId(01) 🎊  theta-testnet-001 => OpenConfirmChannel(OpenConfirm { port_id: transfer, channel_id: channel-4088, connection_id: connection-3594, counterparty_port_id: transfer, counterparty_channel_id: channel-1051 }) at height 0-20881340
2024-03-24T04:01:58.003018Z  INFO ThreadId(01) channel handshake already finished for Channel { ordering: ORDER_UNORDERED, a_side: ChannelSide { chain: BaseChainHandle { chain_id: shielded-expedition.88f17d1d14 }, client_id: 07-tendermint-3257, connection_id: connection-1623, port_id: transfer, channel_id: channel-1051, version: None }, b_side: ChannelSide { chain: BaseChainHandle { chain_id: theta-testnet-001 }, client_id: 07-tendermint-3479, connection_id: connection-3594, port_id: transfer, channel_id: channel-4088, version: None }, connection_delay: 0ns }
SUCCESS Channel {
    ordering: Unordered,
    a_side: ChannelSide {
        chain: BaseChainHandle {
            chain_id: ChainId {
                id: "shielded-expedition.88f17d1d14",
                version: 0,
            },
            runtime_sender: Sender { .. },
        },
        client_id: ClientId(
            "07-tendermint-3257",
        ),
        connection_id: ConnectionId(
            "connection-1623",
        ),
        port_id: PortId(
            "transfer",
        ),
        channel_id: Some(
            ChannelId(
                "channel-1051",
            ),
        ),
        version: None,
    },
    b_side: ChannelSide {
        chain: BaseChainHandle {
            chain_id: ChainId {
                id: "theta-testnet-001",
                version: 0,
            },
            runtime_sender: Sender { .. },
        },
        client_id: ClientId(
            "07-tendermint-3479",
        ),
        connection_id: ConnectionId(
            "connection-3594",
        ),
        port_id: PortId(
            "transfer",
        ),
        channel_id: Some(
            ChannelId(
                "channel-4088",
            ),
        ),
        version: None,
    },
    connection_delay: 0ns,
}
```

### Keys list Namada & Cosmos
```
root@vmi1682379:~# hermes keys list --chain shielded-expedition.88f17d1d14
2024-03-24T04:02:14.897544Z  INFO ThreadId(01) using default configuration from '/root/.hermes/config.toml'
2024-03-24T04:02:14.899350Z  INFO ThreadId(01) running Hermes v1.7.4+38f41c6
SUCCESS 
- thanhphm (tnam1qpr477sufxt3sz800hsgr9xyf3dvc4fjguejd27c)
root@vmi1682379:~# hermes keys list --chain theta-testnet-001
2024-03-24T04:02:22.042554Z  INFO ThreadId(01) using default configuration from '/root/.hermes/config.toml'
2024-03-24T04:02:22.044226Z  INFO ThreadId(01) running Hermes v1.7.4+38f41c6
SUCCESS 
- cosmos-relayer (cosmos1dldemzn0ucxgx5qsh73enh0jlt9p8mkjjsnfxc)
```
### Create Hermes service and start:
```
root@vmi1682379:~# sudo tee /usr/lib/systemd/user/hermesd.service > /dev/null <<EOF
[Unit]
Description=Hermes Daemon Service
After=network.target
StartLimitIntervalSec=60
StartLimitBurst=3

[Service]
Type=simple
Restart=always
RestartSec=20
ExecStart=/usr/local/bin/hermes --config $HOME/.hermes/config.toml start 

[Install]
WantedBy=default.target
EOF
root@vmi1682379:~# sudo chmod 755 /usr/lib/systemd/user/hermesd.service
root@vmi1682379:~# systemctl --user daemon-reload
root@vmi1682379:~# systemctl --user enable hermesd
root@vmi1682379:~# systemctl --user start hermesd
```

### Proof Of IBC Transfer Namada  -> Cosmos:
```
root@vmi1682379:~# namadac --base-dir $BASE_DIR \
    ibc-transfer \
    --amount 5 \
    --source thanhphm \
    --receiver cosmos1dldemzn0ucxgx5qsh73enh0jlt9p8mkjjsnfxc \
    --token NAAN \
    --channel-id channel-1051 \
    --node $RPC_NODE \
    --memo tpknam1qr743g3pjxjm5ywzer9uhss6swk5klthc9cd6qwgxec9jsaq8apvxgcmpy7
Enter your decryption password: 
Transaction added to mempool.
Wrapper transaction hash: E80D2AD97FAA42A3F21FDB2FE544460D1E10D84AC1597D37FAFC99866A70023B
Inner transaction hash: 1887648F2D6444915125AE577A9A62374D0F672CE23DD889783059B24ED699AE
Wrapper transaction accepted at height 211515. Used 26 gas.
Waiting for inner transaction result...
Transaction was successfully applied at height 211516. Used 6193 gas.
```

### Proof Of TXH IBC
- TXH of IBC Create Client on mintscan: [https://www.mintscan.io/cosmoshub-testnet/tx/23D3AB7D2E722F7343426645DEF07BDABF3E41EF7C854E2F79F1148506F9CD24?height=20881303](https://www.mintscan.io/cosmoshub-testnet/tx/23D3AB7D2E722F7343426645DEF07BDABF3E41EF7C854E2F79F1148506F9CD24?height=20881303)
  
- TXH of IBC Channel Open Confirm on mintscan: [https://www.mintscan.io/cosmoshub-testnet/tx/3ED9695E28CA5DFF9C64576AD5B060A6C59B17B0D8E62B63D71BC3BB95F4BCCE?height=20881340](https://www.mintscan.io/cosmoshub-testnet/tx/3ED9695E28CA5DFF9C64576AD5B060A6C59B17B0D8E62B63D71BC3BB95F4BCCE?height=20881340)

- TXH of IBC Transfer 5 NAAN from Namada -> Cosmos on mintscan: [https://www.mintscan.io/cosmoshub-testnet/tx/EAAD177AB75D1AAEE684A3C9A10C60C2F4A6E8477FBFB72961FBE0A520D5D274?height=20882459](https://www.mintscan.io/cosmoshub-testnet/tx/EAAD177AB75D1AAEE684A3C9A10C60C2F4A6E8477FBFB72961FBE0A520D5D274?height=20882459)
