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

# SetMapMode function


## -description


The <b>SetMapMode</b> function sets the mapping mode of the specified device context. The mapping mode defines the unit of measure used to transform page-space units into device-space units, and also defines the orientation of the device's x and y axes.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param iMode

TBD




#### - fnMapMode [in]

The new mapping mode. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MM_ANISOTROPIC"></a><a id="mm_anisotropic"></a><dl>
<dt><b>MM_ANISOTROPIC</b></dt>
</dl>
</td>
<td width="60%">
Logical units are mapped to arbitrary units with arbitrarily scaled axes. Use the <a href="https://msdn.microsoft.com/8fd13d56-f6fa-4aea-a7e5-535caf22a840">SetWindowExtEx</a> and <a href="https://msdn.microsoft.com/36bf82e0-f3e7-43cf-943f-eed783ad24a4">SetViewportExtEx</a> functions to specify the units, orientation, and scaling.

</td>
</tr>
<tr>
<td width="40%"><a id="MM_HIENGLISH"></a><a id="mm_hienglish"></a><dl>
<dt><b>MM_HIENGLISH</b></dt>
</dl>
</td>
<td width="60%">
Each logical unit is mapped to 0.001 inch. Positive x is to the right; positive y is up.

</td>
</tr>
<tr>
<td width="40%"><a id="MM_HIMETRIC"></a><a id="mm_himetric"></a><dl>
<dt><b>MM_HIMETRIC</b></dt>
</dl>
</td>
<td width="60%">
Each logical unit is mapped to 0.01 millimeter. Positive x is to the right; positive y is up.

</td>
</tr>
<tr>
<td width="40%"><a id="MM_ISOTROPIC"></a><a id="mm_isotropic"></a><dl>
<dt><b>MM_ISOTROPIC</b></dt>
</dl>
</td>
<td width="60%">
Logical units are mapped to arbitrary units with equally scaled axes; that is, one unit along the x-axis is equal to one unit along the y-axis. Use the <a href="https://msdn.microsoft.com/8fd13d56-f6fa-4aea-a7e5-535caf22a840">SetWindowExtEx</a> and <a href="https://msdn.microsoft.com/36bf82e0-f3e7-43cf-943f-eed783ad24a4">SetViewportExtEx</a> functions to specify the units and the orientation of the axes. Graphics device interface (GDI) makes adjustments as necessary to ensure the x and y units remain the same size (When the window extent is set, the viewport will be adjusted to keep the units isotropic).

</td>
</tr>
<tr>
<td width="40%"><a id="MM_LOENGLISH"></a><a id="mm_loenglish"></a><dl>
<dt><b>MM_LOENGLISH</b></dt>
</dl>
</td>
<td width="60%">
Each logical unit is mapped to 0.01 inch. Positive x is to the right; positive y is up.

</td>
</tr>
<tr>
<td width="40%"><a id="MM_LOMETRIC"></a><a id="mm_lometric"></a><dl>
<dt><b>MM_LOMETRIC</b></dt>
</dl>
</td>
<td width="60%">
Each logical unit is mapped to 0.1 millimeter. Positive x is to the right; positive y is up.

</td>
</tr>
<tr>
<td width="40%"><a id="MM_TEXT"></a><a id="mm_text"></a><dl>
<dt><b>MM_TEXT</b></dt>
</dl>
</td>
<td width="60%">
Each logical unit is mapped to one device pixel. Positive x is to the right; positive y is down.

</td>
</tr>
<tr>
<td width="40%"><a id="MM_TWIPS"></a><a id="mm_twips"></a><dl>
<dt><b>MM_TWIPS</b></dt>
</dl>
</td>
<td width="60%">
Each logical unit is mapped to one twentieth of a printer's point (1/1440 inch, also called a twip). Positive x is to the right; positive y is up.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value identifies the previous mapping mode.

If the function fails, the return value is zero.




## -remarks



The MM_TEXT mode allows applications to work in device pixels, whose size varies from device to device.

The MM_HIENGLISH, MM_HIMETRIC, MM_LOENGLISH, MM_LOMETRIC, and MM_TWIPS modes are useful for applications drawing in physically meaningful units (such as inches or millimeters).

The MM_ISOTROPIC mode ensures a 1:1 aspect ratio.

The MM_ANISOTROPIC mode allows the x-coordinates and y-coordinates to be adjusted independently.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/61db38d7-9371-4ff1-b96b-1bed4c2a2749">Using Coordinate Spaces and Transformations</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/3ebcabf2-9718-47b2-aba0-7cc28fa42e5a">Coordinate Space and Transformation Functions</a>



<a href="https://msdn.microsoft.com/cfb02788-9b73-4451-9e68-2ad310e0e527">Coordinate Spaces and Transformations Overview</a>



<a href="https://msdn.microsoft.com/bc446b86-3dde-4460-bc54-1eaa4ad19941">GetMapMode</a>



<a href="https://msdn.microsoft.com/36bf82e0-f3e7-43cf-943f-eed783ad24a4">SetViewportExtEx</a>



<a href="https://msdn.microsoft.com/d3b6326e-9fec-42a1-8d2e-d1ad4fcc79a4">SetViewportOrgEx</a>



<a href="https://msdn.microsoft.com/8fd13d56-f6fa-4aea-a7e5-535caf22a840">SetWindowExtEx</a>



<a href="https://msdn.microsoft.com/75409b5a-c003-49f2-aceb-a28330b92b0a">SetWindowOrgEx</a>
 

 

