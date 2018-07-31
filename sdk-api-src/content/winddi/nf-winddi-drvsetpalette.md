---
UID: NF:winddi.DrvSetPalette
title: DrvSetPalette function
author: windows-sdk-content
description: The DrvSetPalette function requests that the driver realize the palette for a specified device.
old-location: display\drvsetpalette.htm
old-project: display
ms.assetid: b7be48e6-188b-4b23-a494-30adcc18f12e
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: DrvSetPalette, DrvSetPalette function [Display Devices], ddifncs_b76ad321-743e-4e7b-bf58-85f969470e29.xml, display.drvsetpalette, winddi/DrvSetPalette
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
 - DrvSetPalette
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DrvSetPalette function


## -description


The <b>DrvSetPalette</b> function requests that the driver realize the palette for a specified device.


## -parameters




### -param dhpdev

Handle to the physical device's <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a> structure, which identifies the device whose palette is to be realized. This parameter is the device handle returned to GDI by <a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>.


### -param ppalo

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff568844">PALOBJ</a> structure from which the colors (RGB values) should be queried.


### -param fl

A set of flags that provides hints and options. This parameter can be the following value:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
SP_DEFAULT

</td>
<td>
The palette is the device's complete default palette. The <a href="https://msdn.microsoft.com/library/windows/hardware/ff568844">PALOBJ</a> can be ignored, but contains the correct contents.

</td>
</tr>
</table>
 


### -param iStart

Specifies the first palette index to overwrite.


### -param cColors

Specifies the number of colors to change in the hardware palette. Extra colors, beyond the number available in the hardware, can be ignored. If <i>cColors</i> is smaller than the size of the hardware palette, set only <i>cColors</i> entries and leave the remaining colors as they are.


## -returns



The return value is <b>TRUE</b> if the function is successful. Otherwise, it is <b>FALSE</b>, and an error code is logged.




## -remarks



 The driver sets the hardware palette to match the entries in the given palette as closely as possible.

Only indexed palettes are realizeable. The RC_PALETTE bit of the <b>flRasterCaps</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff566484">GDIINFO</a> structure specifies whether a device has a realizeable palette.

<b>DrvSetPalette</b> is required for display drivers that support realizeable palettes.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564212">EngCreatePalette</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564808">EngDeletePalette</a>
 

 

