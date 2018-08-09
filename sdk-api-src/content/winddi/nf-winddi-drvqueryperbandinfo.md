---
UID: NF:winddi.DrvQueryPerBandInfo
title: DrvQueryPerBandInfo function
author: windows-sdk-content
description: A printer graphics DLL's DrvQueryPerBandInfo function is called by GDI before it begins drawing a band for a physical page, so the driver can supply GDI with band-specific information.
old-location: display\drvqueryperbandinfo.htm
old-project: display
ms.assetid: 2e2c1aa7-9ba4-4bf9-acfb-43212d3d4899
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: DrvQueryPerBandInfo, DrvQueryPerBandInfo function [Display Devices], ddifncs_8a5e262c-23e5-4e49-bd36-6674efe7090f.xml, display.drvqueryperbandinfo, winddi/DrvQueryPerBandInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Desktop
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
tech.root: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DrvQueryPerBandInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

