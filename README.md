###  DATE: 23/09/2025

###  NAME: KAAMESH M
###  ROLL NO : 212223040080
###  DEPARTMENT: CSE


# EXPERIMENT--02-INTERFACING-A-DIGITAL-INPUT-TO-IOT-DEVELOPMENT-BOARD-
 

## Aim: To Interface a Digital Input  (IR pair ) to ARM IOT development board and write a  program to obtain  the data 
## Components required: STM32 CUBE IDE, ARM IOT development board,  STM programmer tool.
## Theory 
The full form of an ARM is an advanced reduced instruction set computer (RISC) machine, and it is a 32-bit processor architecture expanded by ARM holdings. The applications of an ARM processor include several microcontrollers as well as processors. The architecture of an ARM processor was licensed by many corporations for designing ARM processor-based SoC products and CPUs. This allows the corporations to manufacture their products using ARM architecture. Likewise, all main semiconductor companies will make ARM-based SOCs such as Samsung, Atmel, TI etc.

 
 # IR pair 
 
 ![image](https://user-images.githubusercontent.com/36288975/227598600-730748bf-9884-4a33-95bf-a1fbfde518ed.png)

 IR technology is used in a wide range of wireless applications which includes remote controls and sensing. The infrared part in the electromagnetic spectrum can be separated into three main regions: near IR, mid-IR & far IR. The wavelengths of these three regions vary based on the application. For the near IR region, the wavelength ranges from 700 nm- 1400 nm, the wavelength of the mid-IR region ranges from 1400 nm – 3000 nm & finally for the far IR region, the wavelength ranges from 3000 nm – 1 mm.The near IR region is used on fiber optic & IR sensors, the mid-IR region is used for heat sensing and the far IR region is used in thermal imaging. The range of frequency for IR is maximum as compared to microwave and minimum than visible light.  
## Procedure:
 1. click on STM 32 CUBE IDE, the following screen will appear 
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/4faea5c3-d246-4b0c-ab55-21f16d4d01f3" />

 2. click on FILE, click on new stm 32 project 
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/33b29dba-ca09-40b6-a249-052dedf501ae" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/592576ed-ebf3-43f4-85a6-38b0f6df2e7a" />
3. select the target to be programmed  as shown below and click on next 

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/3e428175-f331-4eaa-bca8-cf7a1e9255ff" />

4.select the program name 

<img width="487" height="538" alt="image" src="https://github.com/user-attachments/assets/0df0d203-9332-4bbd-abee-b7889532410f" />


5. corresponding ioc file will be generated automatically 
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/11ab3368-317c-4fd4-95db-1e1078d25fa5" />

6.select the appropriate pins as gipo, in or out, USART or required options and configure 
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/ae2a22ff-14c6-41c7-9bfe-3e451f50ecdf" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/9fba280f-4d34-4730-afc0-d8a30cfeaa6a" />


7.click on cntrl+S , automaticall C program will be generated 
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/694631f1-9174-4d74-bd77-c7eba356c4ab" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f1aa4d51-953a-48d3-806b-6bf01cbb29a2" />
8. edit the program and as per required 
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/742c7003-0c62-423a-860f-6ddf8986b6fc" />

9. use project and build all 
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/76208543-1d44-4771-89b6-764fb230c16b" />
10. once the project is bulild 
<img width="1088" height="480" alt="image" src="https://github.com/user-attachments/assets/ad427fba-7dfa-4b21-9a40-b1d057c54b70" />

11. click on debug option 
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/885331c0-d143-406d-b413-8a765bda94d0" />

12. connect the  iot board to power supply and usb 

13. After connecting open the STM cube programmer 
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/ce2d4db7-eb67-4727-8d8a-409d162db674" />

14. click on UART and click on connect 
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/de8362f3-d699-424d-8581-0b3b09486eb4" />

15. once it is connected , click on Erasing and programming option 
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/bb6c61cd-fa07-4dac-b702-d39c10745254" />

16. flash the bin or hex file as shown below by switching the switch to flash mode 

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/78b4b6da-76bb-4cd9-9c3d-cfd3cea0b2d5" />


17. check for execution of the output by switching the board to run mode 



## STM 32 CUBE PROGRAM :
```
/* USER CODE BEGIN Header */
/**
  ******************************************************************************
  * @file           : main.c
  * @brief          : Main program body
  ******************************************************************************
  * @attention
  *
  * Copyright (c) 2025 STMicroelectronics.
  * All rights reserved.
  *
  * This software is licensed under terms that can be found in the LICENSE file
  * in the root directory of this software component.
  * If no LICENSE file comes with this software, it is provided AS-IS.
  *
  ******************************************************************************
  */
/* USER CODE END Header */
/* Includes ------------------------------------------------------------------*/
#include "main.h"
#include"stdbool.h"
bool IRSENSOR;
void IRPAIR();
static void MX_GPIO_Init(void);
/* Private includes ----------------------------------------------------------*/
/* USER CODE BEGIN Includes */

/* USER CODE END Includes */

/* Private typedef -----------------------------------------------------------*/
/* USER CODE BEGIN PTD */

/* USER CODE END PTD */

/* Private define ------------------------------------------------------------*/
/* USER CODE BEGIN PD */

/* USER CODE END PD */

/* Private macro -------------------------------------------------------------*/
/* USER CODE BEGIN PM */

/* USER CODE END PM */

/* Private variables ---------------------------------------------------------*/

/* USER CODE BEGIN PV */

/* USER CODE END PV */

/* Private function prototypes -----------------------------------------------*/
void SystemClock_Config(void);
static void MX_GPIO_Init(void);
/* USER CODE BEGIN PFP */

/* USER CODE END PFP */

/* Private user code ---------------------------------------------------------*/
/* USER CODE BEGIN 0 */

/* USER CODE END 0 */

/**
  * @brief  The application entry point.
  * @retval int
  */
int main(void)
{

  /* USER CODE BEGIN 1 */

  /* USER CODE END 1 */

  /* MCU Configuration--------------------------------------------------------*/

  /* Reset of all peripherals, Initializes the Flash interface and the Systick. */
  HAL_Init();

  /* USER CODE BEGIN Init */

  /* USER CODE END Init */

  /* Configure the system clock */
  SystemClock_Config();

  /* USER CODE BEGIN SysInit */

  /* USER CODE END SysInit */

  /* Initialize all configured peripherals */
  MX_GPIO_Init();
  /* USER CODE BEGIN 2 */

  /* USER CODE END 2 */

  /* Infinite loop */
  /* USER CODE BEGIN WHILE */
  while (1)
  {
	  IRPAIR();
    /* USER CODE END WHILE */

    /* USER CODE BEGIN 3 */
  }  /* USER CODE END 3 */
}
void IRPAIR()
{
IRSENSOR = HAL_GPIO_ReadPin(GPIOB,GPIO_PIN_4);
if(IRSENSOR==0)
{
HAL_GPIO_WritePin(GPIOB, GPIO_PIN_5, GPIO_PIN_SET);
HAL_Delay(1000);
HAL_GPIO_WritePin(GPIOB, GPIO_PIN_5, GPIO_PIN_RESET);
HAL_Delay(1000);
}
else
{
HAL_GPIO_WritePin(GPIOB, GPIO_PIN_5, GPIO_PIN_RESET);
HAL_Delay(1000);
}
}
/**
  * @brief System Clock Configuration
  * @retval None
  */
void SystemClock_Config(void)
{
  RCC_OscInitTypeDef RCC_OscInitStruct = {0};
  RCC_ClkInitTypeDef RCC_ClkInitStruct = {0};

  /** Configure the main internal regulator output voltage
  */
  __HAL_PWR_VOLTAGESCALING_CONFIG(PWR_REGULATOR_VOLTAGE_SCALE2);

  /** Initializes the CPU, AHB and APB buses clocks
  */
  RCC_OscInitStruct.OscillatorType = RCC_OSCILLATORTYPE_MSI;
  RCC_OscInitStruct.MSIState = RCC_MSI_ON;
  RCC_OscInitStruct.MSICalibrationValue = RCC_MSICALIBRATION_DEFAULT;
  RCC_OscInitStruct.MSIClockRange = RCC_MSIRANGE_6;
  RCC_OscInitStruct.PLL.PLLState = RCC_PLL_NONE;
  if (HAL_RCC_OscConfig(&RCC_OscInitStruct) != HAL_OK)
  {
    Error_Handler();
  }

  /** Configure the SYSCLKSource, HCLK, PCLK1 and PCLK2 clocks dividers
  */
  RCC_ClkInitStruct.ClockType = RCC_CLOCKTYPE_HCLK3|RCC_CLOCKTYPE_HCLK
                              |RCC_CLOCKTYPE_SYSCLK|RCC_CLOCKTYPE_PCLK1
                              |RCC_CLOCKTYPE_PCLK2;
  RCC_ClkInitStruct.SYSCLKSource = RCC_SYSCLKSOURCE_MSI;
  RCC_ClkInitStruct.AHBCLKDivider = RCC_SYSCLK_DIV1;
  RCC_ClkInitStruct.APB1CLKDivider = RCC_HCLK_DIV1;
  RCC_ClkInitStruct.APB2CLKDivider = RCC_HCLK_DIV1;
  RCC_ClkInitStruct.AHBCLK3Divider = RCC_SYSCLK_DIV1;

  if (HAL_RCC_ClockConfig(&RCC_ClkInitStruct, FLASH_LATENCY_0) != HAL_OK)
  {
    Error_Handler();
  }
}

/**
  * @brief GPIO Initialization Function
  * @param None
  * @retval None
  */
static void MX_GPIO_Init(void)
{
  GPIO_InitTypeDef GPIO_InitStruct = {0};
  /* USER CODE BEGIN MX_GPIO_Init_1 */

  /* USER CODE END MX_GPIO_Init_1 */

  /* GPIO Ports Clock Enable */
  __HAL_RCC_GPIOB_CLK_ENABLE();

  /*Configure GPIO pin Output Level */
  HAL_GPIO_WritePin(GPIOB, GPIO_PIN_5, GPIO_PIN_RESET);

  /*Configure GPIO pin : PB4 */
  GPIO_InitStruct.Pin = GPIO_PIN_4;
  GPIO_InitStruct.Mode = GPIO_MODE_INPUT;
  GPIO_InitStruct.Pull = GPIO_PULLUP;
  HAL_GPIO_Init(GPIOB, &GPIO_InitStruct);

  /*Configure GPIO pin : PB5 */
  GPIO_InitStruct.Pin = GPIO_PIN_5;
  GPIO_InitStruct.Mode = GPIO_MODE_OUTPUT_PP;
  GPIO_InitStruct.Pull = GPIO_NOPULL;
  GPIO_InitStruct.Speed = GPIO_SPEED_FREQ_LOW;
  HAL_GPIO_Init(GPIOB, &GPIO_InitStruct);

  /* USER CODE BEGIN MX_GPIO_Init_2 */

  /* USER CODE END MX_GPIO_Init_2 */
}

/* USER CODE BEGIN 4 */

/* USER CODE END 4 */

/**
  * @brief  This function is executed in case of error occurrence.
  * @retval None
  */
void Error_Handler(void)
{
  /* USER CODE BEGIN Error_Handler_Debug */
  /* User can add his own implementation to report the HAL error return state */
  __disable_irq();
  while (1)
  {
  }
  /* USER CODE END Error_Handler_Debug */
}
#ifdef USE_FULL_ASSERT
/**
  * @brief  Reports the name of the source file and the source line number
  *         where the assert_param error has occurred.
  * @param  file: pointer to the source file name
  * @param  line: assert_param error line source number
  * @retval None
  */
void assert_failed(uint8_t *file, uint32_t line)
{
  /* USER CODE BEGIN 6 */
  /* User can add his own implementation to report the file name and line number,
     ex: printf("Wrong parameters value: file %s on line %d\r\n", file, line) */
  /* USER CODE END 6 */
}
#endif /* USE_FULL_ASSERT */

```



## Output  :
### OFF state
![WhatsApp Image 2025-10-08 at 18 28 18_bc73b512](https://github.com/user-attachments/assets/42797cea-a24b-4c7d-a7f0-48deef0c502b)
 ### ON state
![WhatsApp Image 2025-10-08 at 18 28 18_b9413bf2](https://github.com/user-attachments/assets/a0a637c9-0f1f-49cd-af38-9e70178351fb)

 
 
 
## Result :
Interfacing a digital Input (ir pair) with ARM microcontroller based IOT development is executed and the results are verified.
