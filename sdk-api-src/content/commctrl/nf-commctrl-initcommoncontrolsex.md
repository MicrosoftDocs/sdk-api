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

# InitCommonControlsEx function


## -description


Ensures that the common control DLL (Comctl32.dll) is loaded, and registers specific common control classes from the  DLL. An application must call this function before creating a common control. 


## -parameters




### -param picce

TBD




#### - lpInitCtrls [in]

Type: <b>const LPINITCOMMONCONTROLSEX</b>

A pointer to an <a href="https://msdn.microsoft.com/ad5a1cec-deaf-4011-9313-e79c13e37ce4">INITCOMMONCONTROLSEX</a> structure that contains information specifying which control classes will be registered. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. 




## -remarks




				The effect of each call to <b>InitCommonControlsEx</b> is cumulative. For example, if <b>InitCommonControlsEx</b> is called with the <a href="https://msdn.microsoft.com/ad5a1cec-deaf-4011-9313-e79c13e37ce4">ICC_UPDOWN_CLASS</a> flag, then is later called with the <a href="https://msdn.microsoft.com/ad5a1cec-deaf-4011-9313-e79c13e37ce4">ICC_HOTKEY_CLASS</a> flag, the result is that both the up-down and hot key common control classes are registered and available to the application.
			



