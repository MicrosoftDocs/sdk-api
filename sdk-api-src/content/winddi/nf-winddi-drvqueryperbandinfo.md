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

# DrvQueryPerBandInfo function


## -description


A printer graphics DLL's <b>DrvQueryPerBandInfo</b> function is called by GDI before it begins drawing a band for a physical page, so the driver can supply GDI with band-specific information.


## -parameters




### -param pso [in]

Caller-supplied pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a> structure describing the drawing surface.


### -param pbi [in, out]

Caller-supplied pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff568868">PERBANDINFO</a> structure containing default information, which the function can overwrite.


## -returns



The function must return one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Greater than zero</b></dt>
</dl>
</td>
<td width="60%">
GDI will use the contents of the PERBANDINFO structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Zero</b></dt>
</dl>
</td>
<td width="60%">
GDI will ignore the contents of the PERBANDINFO structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DDI_ERROR</b></dt>
</dl>
</td>
<td width="60%">
GDI will not draw the band.

</td>
</tr>
</table>
 




## -remarks



If a <a href="https://msdn.microsoft.com/58e181ff-c792-41a5-967d-a69a8ff5a041">printer graphics DLL</a> uses GDI-managed surfaces, and if it supports surface banding, it can optionally provide a <b>DrvQueryPerBandInfo</b> function. GDI calls the function prior to rendering each band.

The printer graphics DLL uses the function's <a href="https://msdn.microsoft.com/library/windows/hardware/ff568868">PERBANDINFO</a> structure to indicate whether the previous band should be redrawn, and to specify that the band should be scaled. If a printer graphics DLL supports banding but does not provide a <b>DrvQueryPerBandInfo</b> function, GDI will not repeat or scale bands.

The <b>DrvQueryPerBandInfo</b> function is only called during playback of EMF files.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556250">DrvNextBand</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556292">DrvStartBanding</a>
 

 

