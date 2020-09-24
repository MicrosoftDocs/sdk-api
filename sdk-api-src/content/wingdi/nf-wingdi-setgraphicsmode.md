---
UID: NF:wingdi.SetGraphicsMode
title: SetGraphicsMode function (wingdi.h)
description: The SetGraphicsMode function sets the graphics mode for the specified device context.
helpviewer_keywords: ["GM_ADVANCED","GM_COMPATIBLE","SetGraphicsMode","SetGraphicsMode function [Windows GDI]","_win32_SetGraphicsMode","gdi.setgraphicsmode","wingdi/SetGraphicsMode"]
old-location: gdi\setgraphicsmode.htm
tech.root: gdi
ms.assetid: 73824a14-2951-45a2-98cd-156418c59a2d
ms.date: 12/05/2018
ms.keywords: GM_ADVANCED, GM_COMPATIBLE, SetGraphicsMode, SetGraphicsMode function [Windows GDI], _win32_SetGraphicsMode, gdi.setgraphicsmode, wingdi/SetGraphicsMode
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
 - SetGraphicsMode
 - wingdi/SetGraphicsMode
dev_langs:
 - c++
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
 - SetGraphicsMode
---

# SetGraphicsMode function


## -description

The <b>SetGraphicsMode</b> function sets the graphics mode for the specified device context.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param iMode [in]

The graphics mode. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GM_COMPATIBLE"></a><a id="gm_compatible"></a><dl>
<dt><b>GM_COMPATIBLE</b></dt>
</dl>
</td>
<td width="60%">
Sets the graphics mode that is compatible with 16-bit Windows. This is the default mode. If this value is specified, the application can only modify the world-to-device transform by calling functions that set window and viewport extents and origins, but not by using <a href="/windows/desktop/api/wingdi/nf-wingdi-setworldtransform">SetWorldTransform</a> or <a href="/windows/desktop/api/wingdi/nf-wingdi-modifyworldtransform">ModifyWorldTransform</a>; calls to those functions will fail. Examples of functions that set window and viewport extents and origins are <a href="/windows/desktop/api/wingdi/nf-wingdi-setviewportextex">SetViewportExtEx</a> and <a href="/windows/desktop/api/wingdi/nf-wingdi-setwindowextex">SetWindowExtEx</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GM_ADVANCED"></a><a id="gm_advanced"></a><dl>
<dt><b>GM_ADVANCED</b></dt>
</dl>
</td>
<td width="60%">
Sets the advanced graphics mode that allows world transformations. This value must be specified if the application will set or modify the world transformation for the specified device context. In this mode all graphics, including text output, fully conform to the world-to-device transformation specified in the device context.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is the old graphics mode.

If the function fails, the return value is zero.

## -remarks

There are three areas in which graphics output differs according to the graphics mode:

<ol>
<li>
Text Output: In the GM_COMPATIBLE mode, TrueType (or vector font) text output behaves much the same way as raster font text output with respect to the world-to-device transformations in the DC. The TrueType text is always written from left to right and right side up, even if the rest of the graphics will be flipped on the x or y axis. Only the height of the TrueType (or vector font) text is scaled. The only way to write text that is not horizontal in the GM_COMPATIBLE mode is to specify nonzero escapement and orientation for the logical font selected in this device context.

In the GM_ADVANCED mode, TrueType (or vector font) text output fully conforms to the world-to-device transformation in the device context. The raster fonts only have very limited transformation capabilities (stretching by some integer factors). Graphics device interface (GDI) tries to produce the best output it can with raster fonts for nontrivial transformations.

</li>
<li>
Rectangle Exclusion: If the default GM_COMPATIBLE graphics mode is set, the system excludes bottom and rightmost edges when it draws rectangles.

The GM_ADVANCED graphics mode is required if applications want to draw rectangles that are lower-right inclusive.

</li>
<li>
Arc Drawing: If the default GM_COMPATIBLE graphics mode is set, GDI draws arcs using the current arc direction in the device space. With this convention, arcs do not respect page-to-device transforms that require a flip along the x or y axis.

If the GM_ADVANCED graphics mode is set, GDI always draws arcs in the counterclockwise direction in logical space. This is equivalent to the statement that, in the GM_ADVANCED graphics mode, both arc control points and arcs themselves fully respect the device context's world-to-device transformation.

</li>
</ol>

#### Examples

For an example, see <a href="/windows/desktop/gdi/using-coordinate-spaces-and-transformations">Using Coordinate Spaces and Transformations</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/gdi/coordinate-space-and-transformation-functions">Coordinate Space and Transformation Functions</a>



<a href="/windows/desktop/gdi/coordinate-spaces-and-transformations">Coordinate Spaces and Transformations Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createdca">CreateDC</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getarcdirection">GetArcDirection</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getdc">GetDC</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getgraphicsmode">GetGraphicsMode</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-modifyworldtransform">ModifyWorldTransform</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setarcdirection">SetArcDirection</a>



<b>SetViewportExtEx</b>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setviewportextex">SetViewportExtent</a>



<b>SetWindowExtEx</b>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setwindowextex">SetWindowExtent</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setworldtransform">SetWorldTransform</a>