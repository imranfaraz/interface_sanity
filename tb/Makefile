# Makefile

SIM ?= verilator
TOPLEVEL_LANG ?= verilog

VERILOG_SOURCES = $(wildcard ../rtl/*.sv) tb_interface_sanity.sv

# enable waveform dumping
EXTRA_ARGS += --trace -trace-fst --trace-structs
PLUS_ARGS += --trace -trace-fst --trace-structs

# TOPLEVEL is the name of the toplevel module in your Verilog or VHDL file
TOPLEVEL = tb_interface_sanity

# MODULE is the basename of the Python test file
MODULE = test_interface_sanity

# include cocotb's make rules to take care of the simulator setup
include $(shell cocotb-config --makefiles)/Makefile.sim

clean::
	$(RM) -r __pycache__
	$(RM) results.xml
