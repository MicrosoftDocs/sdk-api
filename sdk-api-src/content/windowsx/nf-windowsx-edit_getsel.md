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

# Edit_GetSel macro


## -description


Gets the starting and ending character positions of the current selection in an edit or rich edit control. You can use this macro or send the <a href="https://msdn.microsoft.com/cf12aaea-cfa7-4804-ae34-fd0992332288">EM_GETSEL</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


## -remarks



This macro does not have the complete functionality of the <a href="https://msdn.microsoft.com/cf12aaea-cfa7-4804-ae34-fd0992332288">EM_GETSEL</a> message, because it does not receive the 32-bit return values in the parameters of <a href="https://msdn.microsoft.com/library/windows/hardware/jj151552">SendMessage</a>.



