---
UID: NF:xinput.XInputGetBatteryInformation
title: XInputGetBatteryInformation function (xinput.h)
description: Retrieves the battery type and charge status of a wireless controller.
helpviewer_keywords: ["XInputGetBatteryInformation","XInputGetBatteryInformation function [XInput Game Controller APIs]","xinput.xinputgetbatteryinformation","xinput/XInputGetBatteryInformation"]
old-location: xinput\xinputgetbatteryinformation.htm
tech.root: xinput
ms.assetid: M:Microsoft.directx_sdk.reference.XInputGetBatteryInformation(DWORD,BYTE,XINPUT_BATTERY_INFORMATION@)
ms.date: 12/05/2018
ms.keywords: XInputGetBatteryInformation, XInputGetBatteryInformation function [XInput Game Controller APIs], xinput.xinputgetbatteryinformation, xinput/XInputGetBatteryInformation
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - XInputGetBatteryInformation
 - xinput/XInputGetBatteryInformation
dev_langs:
 - c++
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

Pointer to an <a href="/windows/desktop/api/xinput/ns-xinput-xinput_battery_information">XINPUT_BATTERY_INFORMATION</a> structure that receives the battery information.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

## -see-also

<a href="/windows/desktop/xinput/functions">XInput Functions</a>