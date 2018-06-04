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

# EngSetLastError function


## -description


The <b>EngSetLastError</b> function causes GDI to report an error code, which can be retrieved by an application. 


## -parameters




### -param Arg1

TBD




#### - iError [in]

Specifies the 32-bit error code to set.


## -returns



None




## -remarks



<b>EngSetLastError</b> sets the last error code for the calling thread. This function allows a driver to communicate error conditions to an application. To facilitate this communication, a driver should use the Win32 application error codes defined in <i>winerror.h</i>.

Only the last error code to be set is retrievable; that is, consecutive calls to <b>EngSetLastError</b> will cause the last-error code field to be overwritten.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564940">EngGetLastError</a>
 

 

