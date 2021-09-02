**CSUN ECE 420**  
-
**Getting Started with bash terminal**  
-
**Name: evan-thomas**  
**Date: september-6th**  

* FPGA  
* VHDL  
* Verilog  

![image](https://user-images.githubusercontent.com/89795951/131444871-6f6b6e98-cb00-4c51-a923-073115d7ef8d.png)  

[Evan Thomas](https://github.com/csun-ece/fa21-e420-assignment0-ce-ET)  
```VHDL
#library ieee;
use ieee.std_logic_1164.all;
use ieee.std_logic_unsigned.all;

entity counter is
    port (
        clk : in std_logic;
        reset : in std_logic;
        enable : in std_logic;
        count : out std_logic_vector(3 downto 0)
    );
end counter;

architecture Behavioral of counter is
    signal pre_count : std_logic_vector(3 downto 0);
begin
    process (clk, enable, reset)
    begin
        if reset = '1' then
            pre_count <= "0000";
        elsif (clk = '1' and clk'event) then
            if enable = '1' then
                pre_count <= pre_count + "1";
            end if;
        end if;
    end process;
    count <= pre_count;
end Behavioral;
```  
![image](https://github.com/csun-ece/fa21-e420-assignment0-ce-ET/blob/master/img/git_stat.png.jpg)

