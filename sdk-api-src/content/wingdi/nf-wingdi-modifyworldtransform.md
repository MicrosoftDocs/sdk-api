---
UID: NF:wingdi.ModifyWorldTransform
title: ModifyWorldTransform function
author: windows-driver-content
description: The ModifyWorldTransform function changes the world transformation for a device context using the specified mode.
old-location: gdi\modifyworldtransform.htm
old-project: gdi
ms.assetid: 2ce070e8-dd6d-4f28-8214-37e825b44273
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: MWT_IDENTITY, MWT_LEFTMULTIPLY, MWT_RIGHTMULTIPLY, ModifyWorldTransform, ModifyWorldTransform function [Windows GDI], _win32_ModifyWorldTransform, gdi.modifyworldtransform, wingdi/ModifyWorldTransform
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
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	gdi32.dll
-	Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
-	GDI32Full.dll
api_name:
-	ModifyWorldTransform
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ModifyWorldTransform function


## -description


The <b>ModifyWorldTransform</b> function changes the world transformation for a device context using the specified mode.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param lpxf

TBD


### -param mode

TBD




#### - iMode [in]

Specifies how the transformation data modifies the current world transformation. This parameter must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MWT_IDENTITY"></a><a id="mwt_identity"></a><dl>
<dt><b>MWT_IDENTITY</b></dt>
</dl>
</td>
<td width="60%">
Resets the current world transformation by using the identity matrix. If this mode is specified, the <a href="https://msdn.microsoft.com/49f0d7ee-77fa-415e-af00-b8930253a3a9">XFORM</a> structure pointed to by <i>lpXform</i> is ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="MWT_LEFTMULTIPLY"></a><a id="mwt_leftmultiply"></a><dl>
<dt><b>MWT_LEFTMULTIPLY</b></dt>
</dl>
</td>
<td width="60%">
Multiplies the current transformation by the data in the <a href="https://msdn.microsoft.com/49f0d7ee-77fa-415e-af00-b8930253a3a9">XFORM</a> structure. (The data in the <b>XFORM</b> structure becomes the left multiplicand, and the data for the current transformation becomes the right multiplicand.)

</td>
</tr>
<tr>
<td width="40%"><a id="MWT_RIGHTMULTIPLY"></a><a id="mwt_rightmultiply"></a><dl>
<dt><b>MWT_RIGHTMULTIPLY</b></dt>
</dl>
</td>
<td width="60%">
Multiplies the current transformation by the data in the <a href="https://msdn.microsoft.com/49f0d7ee-77fa-415e-af00-b8930253a3a9">XFORM</a> structure. (The data in the <b>XFORM</b> structure becomes the right multiplicand, and the data for the current transformation becomes the left multiplicand.)

</td>
</tr>
</table>
 


#### - lpXform [in]

A pointer to an <a href="https://msdn.microsoft.com/49f0d7ee-77fa-415e-af00-b8930253a3a9">XFORM</a> structure used to modify the world transformation for the given device context.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The <b>ModifyWorldTransform</b> function will fail unless graphics mode for the specified device context has been set to GM_ADVANCED by previously calling the <a href="https://msdn.microsoft.com/73824a14-2951-45a2-98cd-156418c59a2d">SetGraphicsMode</a> function. Likewise, it will not be possible to reset the graphics mode for the device context to the default GM_COMPATIBLE mode, unless world transform has first been reset to the default identity transform by calling <a href="https://msdn.microsoft.com/d103a4dd-949e-4f18-ac90-bb0e51011233">SetWorldTransform</a> or <b>ModifyWorldTransform</b>.




## -see-also




<a href="https://msdn.microsoft.com/3ebcabf2-9718-47b2-aba0-7cc28fa42e5a">Coordinate Space and Transformation Functions</a>



<a href="https://msdn.microsoft.com/cfb02788-9b73-4451-9e68-2ad310e0e527">Coordinate Spaces and Transformations Overview</a>



<a href="https://msdn.microsoft.com/72945b1e-144e-4724-bf08-6f971f8adb43">GetWorldTransform</a>



<a href="https://msdn.microsoft.com/73824a14-2951-45a2-98cd-156418c59a2d">SetGraphicsMode</a>



<a href="https://msdn.microsoft.com/d103a4dd-949e-4f18-ac90-bb0e51011233">SetWorldTransform</a>



<a href="https://msdn.microsoft.com/49f0d7ee-77fa-415e-af00-b8930253a3a9">XFORM</a>
 

 

