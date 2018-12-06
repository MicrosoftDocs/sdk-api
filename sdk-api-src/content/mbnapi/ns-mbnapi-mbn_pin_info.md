---
UID: NS:mbnapi.MBN_PIN_INFO
title: MBN_PIN_INFO
author: windows-sdk-content
description: The MBN_PIN_INFO structure represents the current PIN state of the device.
old-location: mbn\mbn_pin_info.htm
tech.root: mbn
ms.assetid: c70b45ea-c16b-4d0d-946a-f543c827c458
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MBN_PIN_INFO, MBN_PIN_INFO structure [Microsoft Broadband Networks], mbn.mbn_pin_info, mbnapi/MBN_PIN_INFO
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mbnapi.h
api_name:
 - MBN_PIN_INFO
product: Windows
targetos: Windows
req.typenames: MBN_PIN_INFO
req.redist: 
---

# MBN_PIN_INFO structure


## -description


The <b>MBN_PIN_INFO</b> structure represents the current PIN state of the device.  It indicates if some PIN is expected by the device and the PIN type expected.  Optionally, it also conveys remaining allowed attempts to enter a valid PIN.  This structure can be obtained by either calling the <a href="https://msdn.microsoft.com/34378403-cf58-4ada-9eb6-f5dad5f69bc9">GetPinState</a> method of <a href="https://msdn.microsoft.com/b5cfabc7-81f8-4ea0-b6f4-5de011320f0b">IMbnPinManager</a> or supplied as an input parameter to the <a href="https://msdn.microsoft.com/6a4bc731-e498-4afb-a648-0b49d2f592ca">OnEnterComplete</a> method of <a href="https://msdn.microsoft.com/4bdaa4e5-880e-4d1f-aec1-36811a0f21c1">IMbnPinEvents</a>. 


## -struct-fields




### -field pinState

An <a href="https://msdn.microsoft.com/5e32e369-2e83-4682-a10c-718f228308ab">MBN_PIN_STATE</a> value that indicates the current PIN state of the device.


### -field pinType

An <a href="https://msdn.microsoft.com/79791522-cf6b-4dae-a9c2-68e9e2fc394f">MBN_PIN_TYPE</a> value that indicates the type of PIN expected.  This field is valid only when <b>pinState</b> is either <b>MBN_PIN_STATE_ENTER</b> or <b>MBN_PIN_STATE_UNBLOCK</b>.


### -field attemptsRemaining

Contains the number of attempts remaining to enter the valid PIN.  This information is not available on some devices.  If it is not available, then it is set to <b>MBN_ATTEMPTS_REMAINING_UNKNOWN</b>.

