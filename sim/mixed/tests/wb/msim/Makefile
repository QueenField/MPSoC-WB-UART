all: build simulate

build:
	if [ ! -e work ]; then vlib work; fi
	vlog -sv +incdir+../../../../rtl/verilog/pkg -f system.verilog.vc
	vcom -2008 -f system.vhdl.vc

simulate:
	vsim -c -do run.do work.mpsoc_uart_testbench
