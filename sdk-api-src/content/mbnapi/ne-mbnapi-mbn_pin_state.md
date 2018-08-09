---
UID: NE:mbnapi.MBN_PIN_STATE
title: MBN_PIN_STATE
author: windows-sdk-content
description: The MBN_PIN_STATE enumerated type indicates the current PIN state of the Mobile Broadband device.
old-location: mbn\mbn_pin_state.htm
old-project: mbn
ms.assetid: 5e32e369-2e83-4682-a10c-718f228308ab
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: MBN_PIN_STATE, MBN_PIN_STATE enumeration [Microsoft Broadband Networks], MBN_PIN_STATE_ENTER, MBN_PIN_STATE_NONE, MBN_PIN_STATE_UNBLOCK, mbn.mbn_pin_state, mbnapi/MBN_PIN_STATE, mbnapi/MBN_PIN_STATE_ENTER, mbnapi/MBN_PIN_STATE_NONE, mbnapi/MBN_PIN_STATE_UNBLOCK
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: MBN_PIN_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mbnapi.h
api_name:
 - MBN_PIN_STATE
product: Windows
targetos: Windows
req.lib: 
req.dll: Mapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# MBN_PIN_STATE enumeration


## -description


The <b>MBN_PIN_STATE</b> enumerated type indicates the current PIN state of the Mobile Broadband device.


## -enum-fields




### -field MBN_PIN_STATE_NONE

Indicates that no PIN is currently required.  

This state can occur when the device does not require a PIN.  It can also occur after repeated PIN entry attempts have exhausted the allowable quota and the device does not allow the PIN to be unblocked programmatically


### -field MBN_PIN_STATE_ENTER

Indicates that the device is currently locked and requires a PIN to be entered to unlock it  The caller can unlock the device by calling the <a href="https://msdn.microsoft.com/71bc0da9-af41-42d6-a7dc-91be54eb6f5c">Enter</a> method of the <a href="https://msdn.microsoft.com/76764dbb-7de0-4b95-a210-60b8e6a4b24b">IMbnPin</a> interface.


### -field MBN_PIN_STATE_UNBLOCK

Indicates that the device is in a PIN blocked state and that the PIN needs to be unblocked using the corresponding PIN Unblock Key (PUK).  The caller can unlock the device by calling the <a href="https://msdn.microsoft.com/7e5ec24c-681c-4259-9f6a-949bf40d5b3e">Unblock</a> method of the <a href="https://msdn.microsoft.com/76764dbb-7de0-4b95-a210-60b8e6a4b24b">IMbnPin</a> interface.

This state can occur after repeated PIN entry attempts have exhausted the allowable quota.

