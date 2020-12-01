---
UID: NF:wingdi.ModifyWorldTransform
title: ModifyWorldTransform function (wingdi.h)
description: The ModifyWorldTransform function changes the world transformation for a device context using the specified mode.
helpviewer_keywords: ["MWT_IDENTITY","MWT_LEFTMULTIPLY","MWT_RIGHTMULTIPLY","ModifyWorldTransform","ModifyWorldTransform function [Windows GDI]","_win32_ModifyWorldTransform","gdi.modifyworldtransform","wingdi/ModifyWorldTransform"]
old-location: gdi\modifyworldtransform.htm
tech.root: gdi
ms.assetid: 2ce070e8-dd6d-4f28-8214-37e825b44273
ms.date: 12/05/2018
ms.keywords: MWT_IDENTITY, MWT_LEFTMULTIPLY, MWT_RIGHTMULTIPLY, ModifyWorldTransform, ModifyWorldTransform function [Windows GDI], _win32_ModifyWorldTransform, gdi.modifyworldtransform, wingdi/ModifyWorldTransform
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ModifyWorldTransform
 - wingdi/ModifyWorldTransform
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - ModifyWorldTransform
---

# ModifyWorldTransform function


## -description

The <b>ModifyWorldTransform</b> function changes the world transformation for a device context using the specified mode.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param lpxf [in]

A pointer to an <a href="/windows/desktop/api/wingdi/ns-wingdi-xform">XFORM</a> structure used to modify the world transformation for the given device context.

### -param mode [in]

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
Resets the current world transformation by using the identity matrix. If this mode is specified, the <a href="/windows/desktop/api/wingdi/ns-wingdi-xform">XFORM</a> structure pointed to by <i>lpXform</i> is ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="MWT_LEFTMULTIPLY"></a><a id="mwt_leftmultiply"></a><dl>
<dt><b>MWT_LEFTMULTIPLY</b></dt>
</dl>
</td>
<td width="60%">
Multiplies the current transformation by the data in the <a href="/windows/desktop/api/wingdi/ns-wingdi-xform">XFORM</a> structure. (The data in the <b>XFORM</b> structure becomes the left multiplicand, and the data for the current transformation becomes the right multiplicand.)

</td>
</tr>
<tr>
<td width="40%"><a id="MWT_RIGHTMULTIPLY"></a><a id="mwt_rightmultiply"></a><dl>
<dt><b>MWT_RIGHTMULTIPLY</b></dt>
</dl>
</td>
<td width="60%">
Multiplies the current transformation by the data in the <a href="/windows/desktop/api/wingdi/ns-wingdi-xform">XFORM</a> structure. (The data in the <b>XFORM</b> structure becomes the right multiplicand, and the data for the current transformation becomes the left multiplicand.)

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The <b>ModifyWorldTransform</b> function will fail unless graphics mode for the specified device context has been set to GM_ADVANCED by previously calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-setgraphicsmode">SetGraphicsMode</a> function. Likewise, it will not be possible to reset the graphics mode for the device context to the default GM_COMPATIBLE mode, unless world transform has first been reset to the default identity transform by calling <a href="/windows/desktop/api/wingdi/nf-wingdi-setworldtransform">SetWorldTransform</a> or <b>ModifyWorldTransform</b>.

## -see-also

<a href="/windows/desktop/gdi/coordinate-space-and-transformation-functions">Coordinate Space and Transformation Functions</a>



<a href="/windows/desktop/gdi/coordinate-spaces-and-transformations">Coordinate Spaces and Transformations Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getworldtransform">GetWorldTransform</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setgraphicsmode">SetGraphicsMode</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setworldtransform">SetWorldTransform</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-xform">XFORM</a>