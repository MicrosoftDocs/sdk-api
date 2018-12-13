---
UID: NF:xinput.XInputGetBatteryInformation
title: XInputGetBatteryInformation function
author: windows-sdk-content
description: Retrieves the battery type and charge status of a wireless controller.
old-location: xinput\xinputgetbatteryinformation.htm
tech.root: xinput
ms.assetid: M:Microsoft.directx_sdk.reference.XInputGetBatteryInformation(DWORD,BYTE,XINPUT_BATTERY_INFORMATION@)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: XInputGetBatteryInformation, XInputGetBatteryInformation function [XInput Game Controller APIs], xinput.xinputgetbatteryinformation, xinput/XInputGetBatteryInformation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: xinput.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Xinput.lib
req.dll: Xinput1_4.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - xinput1_4.dll
 - Ext-MS-Win-Gaming-XInput-L1-1-0.dll
 - xinputuap.dll
api_name:
 - XInputGetBatteryInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XInputGetBatteryInformation function


## -description


Retrieves the battery type and charge status of a wireless controller.


## -parameters




### -param dwUserIndex [in]

Index of the signed-in gamer associated with the device. Can be a value in the range 0–XUSER_MAX_COUNT − 1.


### -param devType [in]

Specifies which device associated with this user index should be queried. Must be <b>BATTERY_DEVTYPE_GAMEPAD</b> or <b>BATTERY_DEVTYPE_HEADSET</b>.


### -param pBatteryInformation [out]

Pointer to an <a href="https://msdn.microsoft.com/2834E5D9-3B7B-46CE-AC40-0C7AB493CAAB">XINPUT_BATTERY_INFORMATION</a> structure that receives the battery information.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.




## -see-also




<a href="https://msdn.microsoft.com/c1533555-9094-0030-f025-6f47e9002e1a">XInput Functions</a>
 

 

