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

# FONTOBJ_vGetInfo function


## -description


The <b>FONTOBJ_vGetInfo</b> function retrieves information about an associated font.


## -parameters




### -param pfo

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a> structure to be queried.


### -param cjSize [in]

Specifies the size in bytes of the buffer pointed to by <i>pfi</i>.


### -param pfi

Pointer to a buffer previously allocated by the driver. GDI writes a <a href="https://msdn.microsoft.com/library/windows/hardware/ff565970">FONTINFO</a> structure to this buffer.


## -returns



None




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff565970">FONTINFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a>
 

 

