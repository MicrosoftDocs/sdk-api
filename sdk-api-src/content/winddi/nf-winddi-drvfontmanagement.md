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

# DrvFontManagement function


## -description


The <b>DrvFontManagement</b> function is an optional entry point provided for PostScript devices. 


## -parameters




### -param pso [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a> structure.


### -param pfo [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a> structure.


### -param iMode [in]

Specifies the escape number to be performed. This must either be equal to QUERYESCSUPPORT (defined in <i>wingdi.h</i>), or in the range 0x100 through 0x3FE.


### -param cjIn [in]

Specifies the size, in bytes, of the buffer pointed to by the <i>pvIn</i> parameter.


### -param pvIn [in]

Pointer to an input buffer. If the <i>iMode</i> parameter is QUERYESCSUPPORT, <i>pvIn</i> points to a ULONG value in the range 0x100 through 0x3FE.


### -param cjOut [in]

Specifies the size, in bytes, of the output buffer pointed to by the <i>pvOut</i> parameter.


### -param pvOut [out]

Pointer to the output data buffer.


## -returns



If this function is hooked by the device driver then GDI will pass calls made by an application to <b>ExtEscape</b> for escape numbers 0x100 through 0x3fe, or for the QUERYESCSUPPORT escape when the first DWORD pointed to by <i>pvIn</i> is in the range 0x100 through 0x3fe.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a>
 

 

