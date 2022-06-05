DRAFT

Admin creates a rewards system

Admin can only adding “users”
An admin is also an user type as well using a flag for admin

ProgramSettings. \
Owner: Pubkey \
AddUser: Pubkey or None (Who can preform actions) \
RemoveUser: Pubkey (Who can preform actions) \
AddItems: Pubkey or None \
VotingTokens: Pubkey or None default admin pub key but when admin makes it to none it cant  \
go back to only admin and voting tokens will go to user who buys the item.

notes: If add user is none anyone can invite - public community. None can't never go to private community. Default: public \
owner can change permissions

User \
Pubkey \
GiveMightifierToken: TokenAccount public key \
ReceiveMightifierToken: TokenAccount public key \
Avatar: collection of avatars

notes: Buy gift modifier token which you can give to others. Receiver person receives GiveMightifierToken that turns into ReceiveMigthifierToken \
ReceiveMightToken can be used to buy avatar. We burn giveMightifierToken 100% and give same 100 RMT.

Item
Owner: Pubkey \
Name: string \
Gratitude: uint64 \
Price (ReceiveMightifierToken): uint64

Store
items: Item[]

notes: store will take ReceiveMigthifierToken and give Item requested.

CommunityPool
ReceiveMightifierToken: Pubkey
Voting: Token

VotingTokens:
All actions done by Admin using Voting Tokens.

notes: In order to burn CommunityPool u need majority of outstanding voting tokens

notes: RMT used to purchase items go to community pool. For now admin owns all the Voting tokens.

OPTIONAL DAO:
Use Solana dao program
