---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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

