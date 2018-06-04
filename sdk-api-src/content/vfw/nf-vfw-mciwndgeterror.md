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

# MCIWndGetError macro


## -description



The <b>MCIWndGetError</b> macro retrieves the last MCI error encountered. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/f110a9b3-5b05-4bf0-85d1-b49ce7396222">MCIWNDM_GETERROR</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param lp

Pointer to an application-defined buffer used to return the error string. 


### -param len

Size, in bytes, of the error buffer. 


## -remarks



If <i>lp</i> is a valid pointer, a null-terminated string corresponding to the error is returned in its buffer. If the error string is longer than the buffer, MCIWnd truncates it.




## -see-also




<a href="https://msdn.microsoft.com/f110a9b3-5b05-4bf0-85d1-b49ce7396222">MCIWNDM_GETERROR</a>
 

 

