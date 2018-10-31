---
UID: NF:wingdi.SetViewportOrgEx
title: SetViewportOrgEx function
author: windows-sdk-content
description: The SetViewportOrgEx function specifies which device point maps to the window origin (0,0).
old-location: gdi\setviewportorgex.htm
tech.root: gdi
ms.assetid: d3b6326e-9fec-42a1-8d2e-d1ad4fcc79a4
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: SetViewportOrgEx, SetViewportOrgEx function [Windows GDI], _win32_SetViewportOrgEx, gdi.setviewportorgex, wingdi/SetViewportOrgEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - SetViewportOrgEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetViewportOrgEx function


## -description


The <b>SetViewportOrgEx</b> function specifies which device point maps to the window origin (0,0).


## -parameters




### -param hdc [in]

A handle to the device context.


### -param x [in]

The x-coordinate, in device units, of the new viewport origin.


### -param y [in]

The y-coordinate, in device units, of the new viewport origin.


### -param lppt [out]

A pointer to a <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure that receives the previous viewport origin, in device coordinates. If <i>lpPoint</i> is <b>NULL</b>, this parameter is not used.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



This function (along with <a href="https://msdn.microsoft.com/36bf82e0-f3e7-43cf-943f-eed783ad24a4">SetViewportExtEx</a> and <a href="https://msdn.microsoft.com/8fd13d56-f6fa-4aea-a7e5-535caf22a840">SetWindowExtEx</a>) helps define the mapping from the logical coordinate space (also known as a <i>window</i>) to the device coordinate space (the <i>viewport</i>). <b>SetViewportOrgEx</b> specifies which device point maps to the logical point (0,0). It has the effect of shifting the axes so that the logical point (0,0) no longer refers to the upper-left corner.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
//map the logical point (0,0) to the device point (xViewOrg, yViewOrg) 
SetViewportOrgEx ( hdc, xViewOrg, yViewOrg, NULL)
</pre>
</td>
</tr>
</table></span></div>
This is related to the <a href="https://msdn.microsoft.com/75409b5a-c003-49f2-aceb-a28330b92b0a">SetWindowOrgEx</a> function. Generally, you will use one function or the other, but not both. Regardless of your use of <b>SetWindowOrgEx</b> and <b>SetViewportOrgEx</b>, the device point (0,0) is always the upper-left corner.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/3407014d-6427-45e9-8be4-b8037ca5438f">Redrawing in the Update Region</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/3ebcabf2-9718-47b2-aba0-7cc28fa42e5a">Coordinate Space and Transformation Functions</a>



<a href="https://msdn.microsoft.com/cfb02788-9b73-4451-9e68-2ad310e0e527">Coordinate Spaces and Transformations Overview</a>



<a href="https://msdn.microsoft.com/6e6c7090-edf4-46a3-8bcd-10a00c0cf847">GetViewportOrgEx</a>



<a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>



<a href="https://msdn.microsoft.com/75409b5a-c003-49f2-aceb-a28330b92b0a">SetWindowOrgEx</a>
 

 

