################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F4xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
sleep_proj.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
sleep_proj.list \

OBJCOPY_BIN += \
sleep_proj.bin \


# All Target
all: sleep_proj.elf secondary-outputs

# Tool invocations
sleep_proj.elf: $(OBJS) $(USER_OBJS) C:\Users\jen\STM32CubeIDE\workspace_1.1.0\sleep_proj\STM32F401RETX_FLASH.ld
	arm-none-eabi-gcc -o "sleep_proj.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"C:\Users\jen\STM32CubeIDE\workspace_1.1.0\sleep_proj\STM32F401RETX_FLASH.ld" --specs=nosys.specs -Wl,-Map="sleep_proj.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

sleep_proj.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "sleep_proj.list"
	@echo 'Finished building: $@'
	@echo ' '

sleep_proj.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "sleep_proj.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
