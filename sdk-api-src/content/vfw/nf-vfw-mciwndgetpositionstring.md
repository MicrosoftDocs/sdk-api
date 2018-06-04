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

# MCIWndGetPositionString macro


## -description



The <b>MCIWndGetPositionString</b> macro retrieves the numerical value of the current position within the content of the MCI device. This macro also provides the current position in string form in an application-defined buffer. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/6dc5d3bd-8515-4514-a2a5-c1bee07f7acf">MCIWNDM_GETPOSITION</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param lp

Pointer to an application-defined buffer used to return the position. Use zero to inhibit retrieval of the position as a string. If the device supports tracks, the string position information is returned in the form TT:MM:SS:FF where TT corresponds to tracks, MM and SS correspond to minutes and seconds, and FF corresponds to frames.



### -param len

Size, in bytes, of the buffer. If the null-terminated string is longer than the buffer, it is truncated. Use zero to inhibit retrieval of the position as a string. 


## -see-also




<a href="https://msdn.microsoft.com/6dc5d3bd-8515-4514-a2a5-c1bee07f7acf">MCIWNDM_GETPOSITION</a>
 

 

