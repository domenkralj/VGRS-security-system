################################################################################
# Automatically-generated file. Do not edit!
# Toolchain: GNU Tools for STM32 (9-2020-q2-update)
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Middlewares/Third_Party/FreeRTOS/Source/portable/MemMang/subdir.mk
-include Middlewares/Third_Party/FreeRTOS/Source/portable/GCC/ARM_CM7/r0p1/subdir.mk
-include Middlewares/Third_Party/FreeRTOS/Source/CMSIS_RTOS_V2/subdir.mk
-include Middlewares/Third_Party/FreeRTOS/Source/subdir.mk
-include Drivers/STM32F7xx_HAL_Driver/Src/subdir.mk
-include Drivers/BSP/STM32F769I-Discovery/subdir.mk
-include Drivers/BSP/Components/wm8994/subdir.mk
-include Drivers/BSP/Components/ts3510/subdir.mk
-include Drivers/BSP/Components/stmpe811/subdir.mk
-include Drivers/BSP/Components/st7789h2/subdir.mk
-include Drivers/BSP/Components/st7735/subdir.mk
-include Drivers/BSP/Components/s5k5cag/subdir.mk
-include Drivers/BSP/Components/ov9655/subdir.mk
-include Drivers/BSP/Components/ov5640/subdir.mk
-include Drivers/BSP/Components/otm8009a/subdir.mk
-include Drivers/BSP/Components/mfxstm32l152/subdir.mk
-include Drivers/BSP/Components/ft6x06/subdir.mk
-include Drivers/BSP/Components/ft5336/subdir.mk
-include Drivers/BSP/Components/exc7200/subdir.mk
-include Drivers/BSP/Components/adv7533/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

OPTIONAL_TOOL_DEPS := \
$(wildcard ../makefile.defs) \
$(wildcard ../makefile.init) \
$(wildcard ../makefile.targets) \


BUILD_ARTIFACT_NAME := vgrs-security-system-stm32f7
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
vgrs-security-system-stm32f7.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
vgrs-security-system-stm32f7.list \

OBJCOPY_BIN += \
vgrs-security-system-stm32f7.bin \


# All Target
all: main-build

# Main-build Target
main-build: vgrs-security-system-stm32f7.elf secondary-outputs

# Tool invocations
vgrs-security-system-stm32f7.elf: $(OBJS) $(USER_OBJS) /Users/domen/STM32CubeIDE/workspace_1.8.0/vgrs-security-system/vgrs-security-system-stm32f7/STM32F769NIHX_FLASH.ld makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-gcc -o "vgrs-security-system-stm32f7.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m7 -T"/Users/domen/STM32CubeIDE/workspace_1.8.0/vgrs-security-system/vgrs-security-system-stm32f7/STM32F769NIHX_FLASH.ld" --specs=nosys.specs -Wl,-Map="vgrs-security-system-stm32f7.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv5-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

vgrs-security-system-stm32f7.list: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "vgrs-security-system-stm32f7.list"
	@echo 'Finished building: $@'
	@echo ' '

vgrs-security-system-stm32f7.bin: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "vgrs-security-system-stm32f7.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) default.size.stdout vgrs-security-system-stm32f7.bin vgrs-security-system-stm32f7.elf vgrs-security-system-stm32f7.list
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents main-build fail-specified-linker-script-missing warn-no-linker-script-specified

-include ../makefile.targets
