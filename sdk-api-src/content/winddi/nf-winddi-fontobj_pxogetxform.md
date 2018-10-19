---
UID: NF:winddi.FONTOBJ_pxoGetXform
title: FONTOBJ_pxoGetXform function
author: windows-sdk-content
description: The FONTOBJ_pxoGetXform function retrieves the notional-to-device transform for the specified font.
old-location: display\fontobj_pxogetxform.htm
tech.root: display
ms.assetid: 94d8ddf6-221f-47f0-8772-4364ad2ac1a2
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: FONTOBJ_pxoGetXform, FONTOBJ_pxoGetXform function [Display Devices], display.fontobj_pxogetxform, gdifncs_22900939-4aa1-4f8b-9345-1d74af8a7f71.xml, winddi/FONTOBJ_pxoGetXform
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - FONTOBJ_pxoGetXform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FONTOBJ_pxoGetXform function


## -description


The <b>FONTOBJ_pxoGetXform</b> function retrieves the notional-to-device transform for the specified font.


## -parameters




### -param pfo

Pointer to the <a href="https://msdn.microsoft.com/09af2006-51f1-433e-9227-3c99b9860e75">FONTOBJ</a> structure for which the transform is to be retrieved.


## -returns



The return value is a pointer to an <a href="https://msdn.microsoft.com/a18af8fc-880a-4ac3-905a-1d9384c2b8d7">XFORMOBJ</a> structure that describes the transform. The XFORMOBJ structure can be used by the <b>XFORMOBJ_</b><b><i>Xxx</i></b> service routines. The XFORMOBJ structure assumes that: 

<ul>
<li>The distance between the pixels is in device space units. </li>
<li>Both notional and device space have positive values of y in the top-to-bottom direction. </li>
</ul>
If the font is a raster font, the return value is <b>NULL</b>.




## -remarks



The driver needs the notional-to-device transform to realize a driver-supplied font.




## -see-also




<a href="https://msdn.microsoft.com/09af2006-51f1-433e-9227-3c99b9860e75">FONTOBJ</a>



<a href="https://msdn.microsoft.com/a18af8fc-880a-4ac3-905a-1d9384c2b8d7">XFORMOBJ</a>
 

 

