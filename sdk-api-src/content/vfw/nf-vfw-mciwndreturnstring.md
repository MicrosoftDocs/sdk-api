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

# MCIWndReturnString macro


## -description



The <b>MCIWndReturnString</b> macro retrieves the reply to the most recent MCI string command sent to an MCI device. Information in the reply is supplied as a null-terminated string. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/36a5222c-a63c-4b8c-ad0c-a00477e95b96">MCIWNDM_RETURNSTRING</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param lp

Pointer to an application-defined buffer to contain the null-terminated string. 


### -param len

Size, in bytes, of the buffer. 


## -remarks



If the null-terminated string is longer than the buffer, the string is truncated.



