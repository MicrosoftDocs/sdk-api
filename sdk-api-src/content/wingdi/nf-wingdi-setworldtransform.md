---
UID: NF:wingdi.SetWorldTransform
title: SetWorldTransform function (wingdi.h)
author: windows-sdk-content
description: The SetWorldTransform function sets a two-dimensional linear transformation between world space and page space for the specified device context. This transformation can be used to scale, rotate, shear, or translate graphics output.
old-location: gdi\setworldtransform.htm
tech.root: gdi
ms.assetid: d103a4dd-949e-4f18-ac90-bb0e51011233
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetWorldTransform, SetWorldTransform function [Windows GDI], _win32_SetWorldTransform, gdi.setworldtransform, wingdi/SetWorldTransform
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
 - Ext-MS-Win-GDI-Draw-l1-1-0.dll
 - Ext-MS-Win-GDI-Draw-l1-1-1.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - SetWorldTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetWorldTransform function


## -description


The <b>SetWorldTransform</b> function sets a two-dimensional linear transformation between world space and page space for the specified device context. This transformation can be used to scale, rotate, shear, or translate graphics output.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param lpxf [in]

A pointer to an <a href="https://msdn.microsoft.com/49f0d7ee-77fa-415e-af00-b8930253a3a9">XFORM</a> structure that contains the transformation data.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



For any coordinates (x, y) in world space, the transformed coordinates in page space (x', y') can be determined by the following algorithm:

<pre class="syntax" xml:space="preserve"><code>x' = x * eM11 + y * eM21 + eDx, 
y' = x * eM12 + y * eM22 + eDy, </code></pre>
where the transformation matrix is represented by the following:

<pre class="syntax" xml:space="preserve"><code>| eM11 eM12 0 | 
| eM21 eM22 0 | 
| eDx  eDy  1 | </code></pre>
This function uses logical units.

The world transformation is usually used to scale or rotate logical images in a device-independent way.

The default world transformation is the identity matrix with zero offset.

The <b>SetWorldTransform</b> function will fail unless the graphics mode for the given device context has been set to GM_ADVANCED by previously calling the <a href="https://msdn.microsoft.com/73824a14-2951-45a2-98cd-156418c59a2d">SetGraphicsMode</a> function. Likewise, it will not be possible to reset the graphics mode for the device context to the default GM_COMPATIBLE mode, unless the world transformation has first been reset to the default identity transformation by calling <b>SetWorldTransform</b> or <a href="https://msdn.microsoft.com/2ce070e8-dd6d-4f28-8214-37e825b44273">ModifyWorldTransform</a>.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/61db38d7-9371-4ff1-b96b-1bed4c2a2749">Using Coordinate Spaces and Transformations</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/3ebcabf2-9718-47b2-aba0-7cc28fa42e5a">Coordinate Space and Transformation Functions</a>



<a href="https://msdn.microsoft.com/cfb02788-9b73-4451-9e68-2ad310e0e527">Coordinate Spaces and Transformations Overview</a>



<a href="https://msdn.microsoft.com/72945b1e-144e-4724-bf08-6f971f8adb43">GetWorldTransform</a>



<a href="https://msdn.microsoft.com/2ce070e8-dd6d-4f28-8214-37e825b44273">ModifyWorldTransform</a>



<a href="https://msdn.microsoft.com/73824a14-2951-45a2-98cd-156418c59a2d">SetGraphicsMode</a>



<a href="https://msdn.microsoft.com/a4d6a63a-6d2d-4bd9-9e71-4cd1b5f145a4">SetMapMode</a>



<a href="https://msdn.microsoft.com/36bf82e0-f3e7-43cf-943f-eed783ad24a4">SetViewportExtEx</a>



<a href="https://msdn.microsoft.com/d3b6326e-9fec-42a1-8d2e-d1ad4fcc79a4">SetViewportOrgEx</a>



<a href="https://msdn.microsoft.com/8fd13d56-f6fa-4aea-a7e5-535caf22a840">SetWindowExtEx</a>



<a href="https://msdn.microsoft.com/75409b5a-c003-49f2-aceb-a28330b92b0a">SetWindowOrgEx</a>



<a href="https://msdn.microsoft.com/49f0d7ee-77fa-415e-af00-b8930253a3a9">XFORM</a>
 

 

