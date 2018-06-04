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

# DrvFree function


## -description


The <b>DrvFree</b> function is used to notify the driver that the specified structure is no longer needed.


## -parameters




### -param pv

Pointer to the structure whose memory is to be freed.


### -param id

Pointer to the identifier that was returned with the structure.


## -returns



None




## -remarks



<b>DrvFree</b> is an optional function that should be supported only if the driver must be informed when memory associated with structures can be freed. For example, if a <a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a> structure is in use, deletion can be deferred until <a href="https://msdn.microsoft.com/library/windows/hardware/ff556192">DrvDestroyFont</a> has been called, eliminating the need for the driver to implement <b>DrvFree</b>.

A driver can use <i>id</i> in different ways. It can specify an object handle or it can indicate the way the structure is allocated. For example, it can differentiate between loaded resources and memory allocated from a heap. The driver can ignore this parameter if the structure pointed to by <i>pv</i> contains enough information.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556192">DrvDestroyFont</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556262">DrvQueryFont</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556266">DrvQueryFontTree</a>
 

 

