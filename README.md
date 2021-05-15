# CRC-implementation
CRC theorem and implementation

# History
A complete data frame :  
         header(frame head) + data + parity bit + frame tail
         
Old method:

  1. odd/even parity check : 
       
       transmitted data "1" number is odd --> parity bit = 1   
      
        ex: 
          transmit data : 00010011   parity bit : 1  --> 000100111
          receive  data : 00100011   parity bit : 1  --> 001000110 (wrong data but it can't be detect when real condtion)
        
  2. checksum
      
        ex:
          transmit data : 01 10 08 20 (Decimal)  checksum = 39 (Decimal)
          rececive data : 08 10 01 20 (Decimal)  checksun = 39 (Decimal) --> (wrong data but it can't be detect when real condtion)


odd/even parity chekc and checksum methods maybe be interfered when data transmits at high speed, and they can't detect error like ours example.  Nowadays, we use CRC in Ethernet/ Data compression/ Video encode /Disk read & write, because its high speed computation and it is easy to desgin in hardware circuit. It is not occur the condition which like odd/even parity check and checksum fatal problem we mention.

# CRC theorem and computation:
  1. 
