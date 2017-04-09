VPATH = src

CUDA_PATH = /usr/local/cuda
CUDA_INC += -I$(CUDA_PATH)/include
NVCC_FLAGS = -Xcompiler -O2 -Xptxas -O2 --compiler-options -Wall -arch=sm_30  --resource-usage
CFLAGS = -O2 -std=c99 -Wall -Wextra

all: pbida c

pbida: pbida.cu
	nvcc -o $@ $(NVCC_FLAGS) $<
c: solverC.c
	gcc -o $@ $(CFLAGS) $<
