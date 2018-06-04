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

# MCIWndGetDevice macro


## -description



The <b>MCIWndGetDevice</b> macro retrieves the name of the current MCI device. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/e69a73a6-a927-4536-98c7-ee7d5b16668a">MCIWNDM_GETDEVICE</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param lp

Pointer to an application-defined buffer to return the device name. 


### -param len

Size, in bytes, of the buffer. 


## -remarks



If the null-terminated string containing the device name is longer than the buffer, MCIWnd truncates it.




## -see-also




<a href="https://msdn.microsoft.com/e69a73a6-a927-4536-98c7-ee7d5b16668a">MCIWNDM_GETDEVICE</a>
 

 

