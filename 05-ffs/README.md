# Lab 5: Samuel Gubi

## Pre-Lab preparation

1. Write characteristic equations and complete truth tables for D, JK, T flip-flops where `q(n)` represents main output value before the clock edge and `q(n+1)` represents output value after the clock edge.   

![Characteristic equations](./rovnice_de1.png)

   **D-type FF**
   | **clk** | **d** | **q(n)** | **q(n+1)** | **Comments** |
   | :-: | :-: | :-: | :-: | :-- |
   | ![rising](./%C5%A1ipka_de1.png) | 0 | 0 | 0 | `q(n+1)` has the same level as `d` |
   | ![rising](./%C5%A1ipka_de1.png) | 0 | 1 | 0 | `q(n+1)` has the same level as `d` |
   | ![rising](./%C5%A1ipka_de1.png) | 1 | 0 | 1 | `q(n+1)` has the same level as `d` |
   | ![rising](./%C5%A1ipka_de1.png) | 1 | 1 | 1 | `q(n+1)` has the same level as `d` |

   **JK-type FF**
   | **clk** | **j** | **k** | **q(n)** | **q(n+1)** | **Comments** |
   | :-: | :-: | :-: | :-: | :-: | :-- |
   | ![rising](./%C5%A1ipka_de1.png) | 0 | 0 | 0 | 0 | Output did not change |
   | ![rising](./%C5%A1ipka_de1.png) | 0 | 0 | 1 | 1 | Output did not change |
   | ![rising](./%C5%A1ipka_de1.png) | 0 | 1 | 0 | 1 | Reset |
   | ![rising](./%C5%A1ipka_de1.png) | 0 | 1 | 0 | 1 | Reset |
   | ![rising](./%C5%A1ipka_de1.png) | 1 | 0 | 1 | 0 | Set |
   | ![rising](./%C5%A1ipka_de1.png) | 1 | 0 | 1 | 0 | Set |
   | ![rising](./%C5%A1ipka_de1.png) | 1 | 1 | 1 | 0 | Toogle |
   | ![rising](./%C5%A1ipka_de1.png) | 1 | 1 | 0 | 1 | Toogle |

   **T-type FF**
   | **clk** | **t** | **q(n)** | **q(n+1)** | **Comments** |
   | :-: | :-: | :-: | :-: | :-- |
   | ![rising](./%C5%A1ipka_de1.png)) | 0 | 0 | 0 | Output did not change |
   | ![rising](./%C5%A1ipka_de1.png) | 0 | 1 | 1 | Output did not change |
   | ![rising](./%C5%A1ipka_de1.png) | 1 | 0 | 1 | Toogle |
   | ![rising](./%C5%A1ipka_de1.png) | 1 | 1 | 0 | Toogle |

<a name="part1"></a>

### D & T Flip-flops

1. Screenshot with simulated time waveforms. Try to simulate both D- and T-type flip-flops in a single testbench with a maximum duration of 200 ns, including reset. Always display all inputs and outputs (display the inputs at the top of the image, the outputs below them) at the appropriate time scale!

   ![your figure]()

### JK Flip-flop

1. Listing of VHDL architecture for JK-type flip-flop. Always use syntax highlighting, meaningful comments, and follow VHDL guidelines:

```vhdl
architecture Behavioral of jk_ff_rst is

    -- WRITE YOUR CODE HERE

    -- Output ports are permanently connected to local signal
    q     <= sig_q;
    q_bar <= not sig_q;
end architecture Behavioral;
```

### Shift register

1. Image of `top` level schematic of the 4-bit shift register. Use four D-type flip-flops and connect them properly. The image can be drawn on a computer or by hand. Always name all inputs, outputs, components and internal signals!

   ![your figure]()

