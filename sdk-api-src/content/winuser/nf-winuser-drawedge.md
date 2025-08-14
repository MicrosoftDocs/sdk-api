---
UID: NF:winuser.DrawEdge
title: DrawEdge function (winuser.h)
description: The DrawEdge function draws one or more edges of rectangle.
helpviewer_keywords: ["BDR_RAISEDINNER","BDR_RAISEDOUTER","BDR_SUNKENINNER","BDR_SUNKENOUTER","BF_ADJUST","BF_BOTTOM","BF_BOTTOMLEFT","BF_BOTTOMRIGHT","BF_DIAGONAL","BF_DIAGONAL_ENDBOTTOMLEFT","BF_DIAGONAL_ENDBOTTOMRIGHT","BF_DIAGONAL_ENDTOPLEFT","BF_DIAGONAL_ENDTOPRIGHT","BF_FLAT","BF_LEFT","BF_MIDDLE","BF_MONO","BF_RECT","BF_RIGHT","BF_SOFT","BF_TOP","BF_TOPLEFT","BF_TOPRIGHT","DrawEdge","DrawEdge function [Windows GDI]","EDGE_BUMP","EDGE_ETCHED","EDGE_RAISED","EDGE_SUNKEN","_win32_DrawEdge","gdi.drawedge","winuser/DrawEdge"]
old-location: gdi\drawedge.htm
tech.root: gdi
ms.assetid: 07d5216e-b577-4ff3-9e3f-eefb486b1ebd
ms.date: 12/05/2018
ms.keywords: BDR_RAISEDINNER, BDR_RAISEDOUTER, BDR_SUNKENINNER, BDR_SUNKENOUTER, BF_ADJUST, BF_BOTTOM, BF_BOTTOMLEFT, BF_BOTTOMRIGHT, BF_DIAGONAL, BF_DIAGONAL_ENDBOTTOMLEFT, BF_DIAGONAL_ENDBOTTOMRIGHT, BF_DIAGONAL_ENDTOPLEFT, BF_DIAGONAL_ENDTOPRIGHT, BF_FLAT, BF_LEFT, BF_MIDDLE, BF_MONO, BF_RECT, BF_RIGHT, BF_SOFT, BF_TOP, BF_TOPLEFT, BF_TOPRIGHT, DrawEdge, DrawEdge function [Windows GDI], EDGE_BUMP, EDGE_ETCHED, EDGE_RAISED, EDGE_SUNKEN, _win32_DrawEdge, gdi.drawedge, winuser/DrawEdge
req.header: winuser.h
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrawEdge
 - winuser/DrawEdge
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-draw-l1-1-0.dll
 - user32.dll
 - ext-ms-win-ntuser-draw-l1-1-2.dll
api_name:
 - DrawEdge
req.apiset: ext-ms-win-ntuser-draw-l1-1-2 (introduced in Windows 10, version 10.0.10240)
---

# DrawEdge function


## -description

The <b>DrawEdge</b> function draws one or more edges of rectangle.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param qrc [in, out]

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the logical coordinates of the rectangle.

### -param edge [in]

The type of inner and outer edges to draw. This parameter must be a combination of one inner-border flag and one outer-border flag. The inner-border flags are as follows.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BDR_RAISEDINNER"></a><a id="bdr_raisedinner"></a><dl>
<dt><b>BDR_RAISEDINNER</b></dt>
</dl>
</td>
<td width="60%">
Raised inner edge.

</td>
</tr>
<tr>
<td width="40%"><a id="BDR_SUNKENINNER"></a><a id="bdr_sunkeninner"></a><dl>
<dt><b>BDR_SUNKENINNER</b></dt>
</dl>
</td>
<td width="60%">
Sunken inner edge.

</td>
</tr>
</table>
 

The outer-border flags are as follows.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BDR_RAISEDOUTER"></a><a id="bdr_raisedouter"></a><dl>
<dt><b>BDR_RAISEDOUTER</b></dt>
</dl>
</td>
<td width="60%">
Raised outer edge.

</td>
</tr>
<tr>
<td width="40%"><a id="BDR_SUNKENOUTER"></a><a id="bdr_sunkenouter"></a><dl>
<dt><b>BDR_SUNKENOUTER</b></dt>
</dl>
</td>
<td width="60%">
Sunken outer edge.

</td>
</tr>
</table>
 

Alternatively, the <i>edge</i> parameter can specify one of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EDGE_BUMP"></a><a id="edge_bump"></a><dl>
<dt><b>EDGE_BUMP</b></dt>
</dl>
</td>
<td width="60%">
Combination of BDR_RAISEDOUTER and BDR_SUNKENINNER.

</td>
</tr>
<tr>
<td width="40%"><a id="EDGE_ETCHED"></a><a id="edge_etched"></a><dl>
<dt><b>EDGE_ETCHED</b></dt>
</dl>
</td>
<td width="60%">
Combination of BDR_SUNKENOUTER and BDR_RAISEDINNER.

</td>
</tr>
<tr>
<td width="40%"><a id="EDGE_RAISED"></a><a id="edge_raised"></a><dl>
<dt><b>EDGE_RAISED</b></dt>
</dl>
</td>
<td width="60%">
Combination of BDR_RAISEDOUTER and BDR_RAISEDINNER.

</td>
</tr>
<tr>
<td width="40%"><a id="EDGE_SUNKEN"></a><a id="edge_sunken"></a><dl>
<dt><b>EDGE_SUNKEN</b></dt>
</dl>
</td>
<td width="60%">
Combination of BDR_SUNKENOUTER and BDR_SUNKENINNER.

</td>
</tr>
</table>

### -param grfFlags [in]

The type of border. This parameter can be a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BF_ADJUST"></a><a id="bf_adjust"></a><dl>
<dt><b>BF_ADJUST</b></dt>
</dl>
</td>
<td width="60%">
If this flag is passed, shrink the rectangle pointed to by the <i>qrc</i> parameter to exclude the edges that were drawn.

If this flag is not passed, then do not change the rectangle pointed to by the <i>qrc</i> parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="BF_BOTTOM"></a><a id="bf_bottom"></a><dl>
<dt><b>BF_BOTTOM</b></dt>
</dl>
</td>
<td width="60%">
Bottom of border rectangle.

</td>
</tr>
<tr>
<td width="40%"><a id="BF_BOTTOMLEFT"></a><a id="bf_bottomleft"></a><dl>
<dt><b>BF_BOTTOMLEFT</b></dt>
</dl>
</td>
<td width="60%">
Bottom and left side of border rectangle.

</td>
</tr>
<tr>
<td width="40%"><a id="BF_BOTTOMRIGHT"></a><a id="bf_bottomright"></a><dl>
<dt><b>BF_BOTTOMRIGHT</b></dt>
</dl>
</td>
<td width="60%">
Bottom and right side of border rectangle.

</td>
</tr>
<tr>
<td width="40%"><a id="BF_DIAGONAL"></a><a id="bf_diagonal"></a><dl>
<dt><b>BF_DIAGONAL</b></dt>
</dl>
</td>
<td width="60%">
Diagonal border.

</td>
</tr>
<tr>
<td width="40%"><a id="BF_DIAGONAL_ENDBOTTOMLEFT"></a><a id="bf_diagonal_endbottomleft"></a><dl>
<dt><b>BF_DIAGONAL_ENDBOTTOMLEFT</b></dt>
</dl>
</td>
<td width="60%">
Diagonal border. The end point is the lower-left corner of the rectangle; the origin is top-right corner.

</td>
</tr>
<tr>
<td width="40%"><a id="BF_DIAGONAL_ENDBOTTOMRIGHT"></a><a id="bf_diagonal_endbottomright"></a><dl>
<dt><b>BF_DIAGONAL_ENDBOTTOMRIGHT</b></dt>
</dl>
</td>
<td width="60%">
Diagonal border. The end point is the lower-right corner of the rectangle; the origin is top-left corner.

</td>
</tr>
<tr>
<td width="40%"><a id="BF_DIAGONAL_ENDTOPLEFT"></a><a id="bf_diagonal_endtopleft"></a><dl>
<dt><b>BF_DIAGONAL_ENDTOPLEFT</b></dt>
</dl>
</td>
<td width="60%">
Diagonal border. The end point is the top-left corner of the rectangle; the origin is lower-right corner.

</td>
</tr>
<tr>
<td width="40%"><a id="BF_DIAGONAL_ENDTOPRIGHT"></a><a id="bf_diagonal_endtopright"></a><dl>
<dt><b>BF_DIAGONAL_ENDTOPRIGHT</b></dt>
</dl>
</td>
<td width="60%">
Diagonal border. The end point is the top-right corner of the rectangle; the origin is lower-left corner.

</td>
</tr>
<tr>
<td width="40%"><a id="BF_FLAT"></a><a id="bf_flat"></a><dl>
<dt><b>BF_FLAT</b></dt>
</dl>
</td>
<td width="60%">
Flat border.

</td>
</tr>
<tr>
<td width="40%"><a id="BF_LEFT"></a><a id="bf_left"></a><dl>
<dt><b>BF_LEFT</b></dt>
</dl>
</td>
<td width="60%">
Left side of border rectangle.

</td>
</tr>
<tr>
<td width="40%"><a id="BF_MIDDLE"></a><a id="bf_middle"></a><dl>
<dt><b>BF_MIDDLE</b></dt>
</dl>
</td>
<td width="60%">
Interior of rectangle to be filled.

</td>
</tr>
<tr>
<td width="40%"><a id="BF_MONO"></a><a id="bf_mono"></a><dl>
<dt><b>BF_MONO</b></dt>
</dl>
</td>
<td width="60%">
One-dimensional border.

</td>
</tr>
<tr>
<td width="40%"><a id="BF_RECT"></a><a id="bf_rect"></a><dl>
<dt><b>BF_RECT</b></dt>
</dl>
</td>
<td width="60%">
Entire border rectangle.

</td>
</tr>
<tr>
<td width="40%"><a id="BF_RIGHT"></a><a id="bf_right"></a><dl>
<dt><b>BF_RIGHT</b></dt>
</dl>
</td>
<td width="60%">
Right side of border rectangle.

</td>
</tr>
<tr>
<td width="40%"><a id="BF_SOFT"></a><a id="bf_soft"></a><dl>
<dt><b>BF_SOFT</b></dt>
</dl>
</td>
<td width="60%">
Soft buttons instead of tiles.

</td>
</tr>
<tr>
<td width="40%"><a id="BF_TOP"></a><a id="bf_top"></a><dl>
<dt><b>BF_TOP</b></dt>
</dl>
</td>
<td width="60%">
Top of border rectangle.

</td>
</tr>
<tr>
<td width="40%"><a id="BF_TOPLEFT"></a><a id="bf_topleft"></a><dl>
<dt><b>BF_TOPLEFT</b></dt>
</dl>
</td>
<td width="60%">
Top and left side of border rectangle.

</td>
</tr>
<tr>
<td width="40%"><a id="BF_TOPRIGHT"></a><a id="bf_topright"></a><dl>
<dt><b>BF_TOPRIGHT</b></dt>
</dl>
</td>
<td width="60%">
Top and right side of border rectangle.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -see-also

<a href="/windows/desktop/gdi/painting-and-drawing-functions">Painting and Drawing Functions</a>



<a href="/windows/desktop/gdi/painting-and-drawing">Painting and Drawing Overview</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT
      </a>
