# Auction_smart_contract

The Auction Smart Contract
1. Smart Contract for a Decentralized Auction like an eBay alternative;
2. The Auction has an owner (the person who sells a good or service), a start and an end date;
3. The owner can cancel the auction if there is an emergency or can finalize the auction after its end time;
4. People are sending ETH by calling a function called placeBid(). The sender’s address and the value sent to the auction will be stored in mapping variable called bids;
5. Users are incentivized to bid the maximum they’re willing to pay, but they are not bound to that full amount, but rather to the previous highest bid plus an increment. The contract will automatically bid up to a given amount;
6. The highestBindingBid is the selling price and the highestBidder the person who won the auction;
7. After the auction ends the owner gets the highestBindingBid and everybody else
   
The Auction Contract - The placeBid() function
1. bids[0x123...] = 40
2. bids[0xabc...] = 70
3. bidIncrement = 10
4. highestBidder = 0xabc...
5. highestBindingBid = 50 
---------------------------------------------
1. 0x123... is sending 100 wei
2. bids[0x123...] = 40 + 100= 140 
3. highestBindingBid = min(140, 70+10) = 80
