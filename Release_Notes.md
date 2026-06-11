

# Release Notes for <mark>\ STM32U5xx CMSIS </mark>
Copyright &copy; 2021\ STMicroelectronics\
    
[![ST logo](_htmresc/st_logo_2020.png)](https://www.st.com)



# __Update History__

<label for="collapse-section10" checked aria-hidden="true">__V1.4.3 / 03-June-2026__</label>
<div>

## Main Changes 
  - Align RNG NIST compliance values with the RNG register values defined in the application note.
  - Remove the I2C_CR1_SWRST bit macros.
  - Set stack limit (MSPLIM) in CMSIS Device templates.
  - Fix wrong comments related to RCC_CCIPR3 masks in stm32u5x5xx.h files.
  - Fix wrong comments at the head of startup_stm32u535/45xx.s files.

## Backward Compatibility
- N/A

</div>

<label for="collapse-section9" checked aria-hidden="true">__V1.4.2 / 04-June-2025__</label>
<div>

## Main Changes 
  - General updates to fix known defects and implementation enhancements.
  - Remove the internal CRC registers from defined CMSIS CRC structure (CRC_TypeDef).
  - Allow redefinition of the macro 'VECT_TAB_OFFSET' externally from the IDE, makefile, or command line.
  - Align the JPEG base address in Secure mode with the one defined for Non-Secure mode.
  - Add specific gcc linker files for STM32U5A5xx devices.
  - Increase the total SRAM size in STM32U5G9 linker file template to include SRAM6 size.

## Backward Compatibility
- N/A

</div>

<label for="collapse-section8" aria-hidden="true">__V1.4.1 / 30-October-2024__</label>
<div>

## Main Changes 
  - General updates to fix known defects and implementation enhancements.
  - Fix TAMP_CR3_ITAMP7NOER bit definition to be aligned with reference manual.
  - Add missing USB_OTG_GINTSTS_RSTDET bit definition.
  - Align USB OTG bit definition with reference manual.


## Backward Compatibility
- N/A

</div>

<label for="collapse-section7" checked aria-hidden="true">__V1.4.0 / 13-February-2024__</label>
<div>

## Main Changes 

**CMSIS Device** Maintenance Release version of bits and registers definition aligned with RM0456 (STM32U5 reference manual)

  - Add Bits definition for RNG_NSCR register for RNG noise source control
  - Rename RTC_CR_ALRAOCLR to RTC_CR_ALRAFCLR definition
  - Rename RTC_CR_ALRBOCLR to RTC_CR_ALRBFCLR definition
  - Remove SYSCFG_UCPD_CC1ENRXFILTER and SYSCFG_UCPD_CC2ENRXFILTER defines
  - Remove COMP2 dependency in "stm32u545xx.h" and "stm32u545xx.h" files by removing TIM1_AF1_BKCMP2E, TIM1_AF1_BKCMP2P, TIM1_AF2_BK2CMP2E and TIM1_AF2_BK2CMP2P defines 
  - Remove PWR_PDCRI register in "stm32u545xx.h" and "stm32u545xx.h" files by removing PWR_PDCRI_PD0, PWR_PDCRI_PD1, PWR_PDCRI_PD2, PWR_PDCRI_PD3, PWR_PDCRI_PD4, PWR_PDCRI_PD5, PWR_PDCRI_PD6 and PWR_PDCRI_PD0 defines 
  - Update **partition_stm32u5XXxx.h** files headers
  - Fix wrong declaration of g_pfnVectors size in GCC **startup_stm32u5XXxx.s** files
  - Update linker files to properly mark sections readonly for GCC12


## Backward Compatibility
- N/A

</div>

<label for="collapse-section6" checked aria-hidden="true">__V1.3.1 / 20-October-2023__</label>
<div>

## Main Changes 

**CMSIS Device** Official Release version of bits and registers definition aligned with RM0456 (STM32U5 reference manual)

  - Update STM32U5A5xx devices list with STM32U5A5QII3Q under "stm32u5xx.h” file



## Backward Compatibility
- N/A

</div>


<label for="collapse-section5" checked aria-hidden="true">__V1.3.0 / 09-June-2023__</label>
<div>

## Main Changes 

**CMSIS Device** Official Release version of bits and registers definition aligned with RM0456 (STM32U5 reference manual)

- **Support of new STM32U5F9xx, STM32U5G9xx, STM32U5F7xx and STM32U5G7xx devices**:
  - Add “stm32u5f9xx.h”, “stm32u5g9xx.h”, “stm32u5f7xx.h” and “stm32u5g7xx.h” files
  - Add startup files “startup_stm32u5f9xx.s”, “startup_stm32u5g9xx.s”, “startup_stm32u5f7xx.s” and “startup_stm32u5g7xx.s” for EWARM, STM32CubeIDE and MDK-ARM toolchains
  - Add linker files for EWARM and STM32CubeIDE toolchains of STM32U5F9xx/STM32U5G9xx/STM32U5F7xx/STM32U5G7xx devices


## Backward Compatibility
- N/A

</div>


<label for="collapse-section4" checked aria-hidden="true">__V1.2.0 / 08-June-2023__</label>
<div>

## Main Changes 

**CMSIS Device** Official Release version of bits and registers definition aligned with RM0456 (STM32U5 reference manual)

- **Support of stm32u535xx and stm32u545xx devices**:
  - Add "stm32u535xx.h" and "stm32u545xx.h" files
  - Add startup files "startup_stm32u535xx.s" and "startup_stm32u545xx.s" for EWARM and STM32CUBEIDE toolchains
  - Add EWARM and STM32CUBEIDE linker files for all devices for legacy and for TrustZone based application

- **Registers and bit field definitions updates**:

  - Add USB Dual Role Device FS Endpoint registers:
    - Add Bits definition for USB_DRD_CNTR register
    - Add Bits definition for USB_DRD_ISTR register
    - Add Bits definition for USB_DRD_FNR register
    - Add Bits definition for USB_DRD_DADDR register
    - Add Bit definition for USB_DRD_BTABLE register 
    - Add Bit definition for LPMCSR register
    - Add Bits definition for USB_DRD_BCDR register
    - Add Bits definition for USB_DRD_CHEP register
  - Add USB_IRQn interrupt
  - Add USB_OTG_GCCFG_PULLDOWNEN define
  - Add LSECSSD and MSI_PLL_UNLOCK global interrupts
  - Add USART_DMAREQUESTS_SW_WA define
  - Add DBGMCU_APB1FZR2_DBG_I2C5_STOP and DBGMCU_APB1FZR2_DBG_I2C6_STOP defines
  - Remove DBGMCU_APB1FZR2_DBG_FDCAN_STOP define
  - Add AES_IER_RNGEIE AES_ICR_RNGEIF and AES_ISR_RNGEIF defines
  - Add DMA2D_TRIGGER_SUPPORT define
  - Rename Bit definition for EXTI_SECENR1 register to EXTI_SECCFGR1 register
  - Rename Bit definition for EXTI_PRIVENR1 register to EXTI_PRIVCFGR1 register
  - Add Bit definition for EXTI_LOCKR register
  - Add EXTI_RTSR1_RT25, EXTI_FTSR1_FT25, EXTI_SWIER1_SWI25, EXTI_RPR1_RPIF25, EXTI_FPR1_FPIF25, EXTI_IMR1_IM25 and EXTI_EMR1_EM25 defines
  - Add COMP_WINDOW_MODE_SUPPORT define
  - Add Bit definition for SYSCFG_OTGHSPHYTUNER2 register
  - Add SYSCFG_CFGR1_SRAMCACHED define
  - Add UCPD configuration register 3
  - Add RCC_APB2RSTR_USBRST define
  - Add RCC_APB2ENR_USBEN define
  - Add RCC_APB2SMENR_USBSMEN define
  - Add IS_SPI_GRP1_INSTANCE and IS_SPI_GRP2_INSTANCE macros
  - Add IS_COMP_ALL_INSTANCE macro
  - Add IS_HCD_ALL_INSTANCE and IS_PCD_ALL_INSTANCE macro
  - Add PWR_CR1_FORCE_USBPWR and PWR_VOSR_VDD11USBDIS defines
  - Rename OCTOSPI_CR_DQM to XSPI_CR_DMM
  - Rename OCTOSPI_CR_FSEL to XSPI_OCTOSPI_CR_MSEL
  - Rename ADC4_PW_AUTOFF to ADC4_PWRR_AUTOFF
  - Rename ADC4_PW_DPD to ADC4_PWRR_DPD
  - Rename ADC4_PW_VREFPROT to ADC4_PWRR_VREFPROT
  - Rename ADC4_PW_VREFSECSMP to ADC4_PWRR_VREFSECSMP

## Backward Compatibility
- N/A

</div>


<label for="collapse-section3" checked aria-hidden="true">__V1.1.0 /  16-February-2022__</label>
<div>

## Main Changes 

- **CMSIS Device** Maintenance Release version of bits and registers definition aligned with RM0456 (STM32U5 reference manual)
  - Add the support of STM32U595xx, STM32U5A5xx, STM32U599xx and STM32U5A9xx devices
  - Define XSPI_TypeDef as alias to OCTOSPI_TypeDef and HSPI_TypeDef
  - Define XSPIM_TypeDef as alias to OCTOSPIM_TypeDef
  - Update XSPI bit definition to alias OCTOSPI and HSPI bits
  - Add OPAMP12_COMMON_NS, OPAMP12_COMMON_S, OPAMP12_COMMON, OPAMP12_COMMON_BASE defines
  - Update OPAMP_Common_TypeDef to align with reference manual
  - Add the SRAM4 memory definition in all STM32CubeIDE flashloader files
  - Update the flash size define to support:
     - STM32U575/STM32U585: 2Mbytes flash devices
     - STM32U595/STM32U5A5/STM32U599/STM32U5A9: 4Mbytes flash devices
  - Rename PVD_AVD_IRQHandler to PVD_PVM_IRQHandler in all start-up files
  - Rename RCC_AHB2RSTR1_ADC1RST to RCC_AHB2RSTR1_ADC12RST
  - Rename RCC_AHB2ENR1_ADC1EN to RCC_AHB2ENR1_ADC12EN
  - Rename RCC_AHB2SMENR1_ADC1SMEN to RCC_AHB2SMENR1_ADC12SMEN
  - Rename RCC_CCIPR1_CLK48MSEL to RCC_CCIPR1_ICLKSEL
  - Rename RCC_SECCFGR_CLK48MSEC to RCC_SECCFGR_ICLKSEC
  - Add TIM3 and TIM4 are missing in IS_TIM_32B_COUNTER_INSTANCE macro definition

</div>

<label for="collapse-section2" checked aria-hidden="true">__V1.0.1 /  01-October-2021__</label>
<div>

## Main Changes 

- Rename OTG_FS_BASE_NS to USB_OTG_FS_BASE_NS define
- Rename OTG_FS_BASE_S to USB_OTG_FS_BASE_S define
- Add LSI_STARTUP_TIME define
- Fix wrong IRQn name in partition_stm32u5xx.h


</div>


<label for="collapse-section1" checked aria-hidden="true">__V1.0.0 /  28-June-2021__</label>
<div>

## Main Changes 

- First official release version of bits and registers definition aligned with RM0456 (STM32U5 reference manual)


</div>


For complete documentation on STM32 Microcontrollers </mark> ,
visit: http://www.st.com/stm32