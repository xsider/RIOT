APPLICATION = driver_mma8652
include ../Makefile.tests_common

FEATURES_REQUIRED = periph_i2c

USEMODULE += mma8652
USEMODULE += xtimer

ifneq (,$(TEST_MMA8652_I2C))
  CFLAGS += -DTEST_MMA8652_I2C=$(TEST_MMA8652_I2C)
else
  CFLAGS += -DTEST_MMA8652_I2C=I2C_0
endif
ifneq (,$(TEST_MMA8652_ADDR))
  CFLAGS += -DTEST_MMA8652_ADDR=$(TEST_MMA8652_ADDR)
else
  CFLAGS += -DTEST_MMA8652_ADDR=0x1D
endif

ifneq (,$(TEST_MMA8652_USER_OFFSET_X))
  CFLAGS += -DTEST_MMA8652_USER_OFFSET_X=$(TEST_MMA8652_USER_OFFSET_X)
else
  CFLAGS += -DTEST_MMA8652_USER_OFFSET_X=0
endif
ifneq (,$(TEST_MMA8652_USER_OFFSET_Y))
  CFLAGS += -DTEST_MMA8652_USER_OFFSET_Y=$(TEST_MMA8652_USER_OFFSET_Y)
else
  CFLAGS += -DTEST_MMA8652_USER_OFFSET_Y=0
endif
ifneq (,$(TEST_MMA8652_USER_OFFSET_Z))
  CFLAGS += -DTEST_MMA8652_USER_OFFSET_Z=$(TEST_MMA8652_USER_OFFSET_Z)
else
  CFLAGS += -DTEST_MMA8652_USER_OFFSET_Z=0
endif

include $(RIOTBASE)/Makefile.include
