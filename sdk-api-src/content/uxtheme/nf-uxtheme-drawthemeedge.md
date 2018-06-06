---
UID: NF:uxtheme.DrawThemeEdge
title: DrawThemeEdge function
author: windows-sdk-content
description: Draws one or more edges defined by the visual style of a rectangle.
old-location: controls\DrawThemeEdge.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\drawthemeedge.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: DrawThemeEdge, DrawThemeEdge function [Windows Controls], controls.DrawThemeEdge, controls.inet_DrawThemeEdge, inet_DrawThemeEdge, inet_DrawThemeEdge_cpp, uxtheme/DrawThemeEdge
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: uxtheme.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: BP_BUFFERFORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - UxTheme.dll
api_name:
 - DrawThemeEdge
product: Windows
targetos: Windows
req.lib: UxTheme.lib
req.dll: UxTheme.dll
req.irql: 
req.product: Windows UI
---

# DrawThemeEdge function


## -description


Draws one or more edges defined by the visual style of a rectangle.


## -parameters




### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="https://msdn.microsoft.com/3c496a3f-e4d0-4938-af66-85df93829cd8">OpenThemeData</a> to create an HTHEME.


### -param hdc [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

HDC.


### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part that contains the rectangle. See <a href="https://msdn.microsoft.com/97740fb8-c393-4c12-b5ef-9285220117f0">Parts and States</a>.


### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part. See <a href="https://msdn.microsoft.com/97740fb8-c393-4c12-b5ef-9285220117f0">Parts and States</a>.


### -param pDestRect [in]

Type: <b>LPCRECT</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that contains, in logical coordinates, the rectangle.


### -param uEdge [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

<b>UINT</b> that specifies the type of inner and outer edges to draw. This parameter must be a combination of one inner-border flag and one outer-border flag, or one of the combination flags. The border flags are:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>BDR_RAISEDINNER</dt>
</dl>
</td>
<td width="60%">
Raised inner edge

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>BDR_SUNKENINNER</dt>
</dl>
</td>
<td width="60%">
Sunken inner edge

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>BDR_RAISEDOUTER</dt>
</dl>
</td>
<td width="60%">
Raised outer edge

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>BDR_SUNKENOUTER</dt>
</dl>
</td>
<td width="60%">
Sunken outer edge

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>EDGE_BUMP</dt>
</dl>
</td>
<td width="60%">
Combination of BDR_RAISEDOUTER and BDR_SUNKENINNER

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>EDGE_ETCHED</dt>
</dl>
</td>
<td width="60%">
Combination of BDR_SUNKENOUTER and BDR_RAISEDINNER

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>EDGE_RAISED</dt>
</dl>
</td>
<td width="60%">
Combination of BDR_RAISEDOUTER and BDR_RAISEDINNER

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>EDGE_SUNKEN</dt>
</dl>
</td>
<td width="60%">
Combination of BDR_SUNKENOUTER and BDR_SUNKENINNER

</td>
</tr>
</table>
 


### -param uFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

<b>UINT</b> that specifies the type of border to draw. This parameter can be a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>BF_ADJUST</dt>
</dl>
</td>
<td width="60%">
The rectangle pointed to by the <i>pDestRect</i> parameter is shrunk to exclude the edges that were drawn; otherwise the rectangle does not change.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>BF_BOTTOM</dt>
</dl>
</td>
<td width="60%">
Bottom of border rectangle.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>BF_BOTTOMLEFT</dt>
</dl>
</td>
<td width="60%">
Bottom and left side of border rectangle.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>BF_BOTTOMRIGHT</dt>
</dl>
</td>
<td width="60%">
Bottom and right side of border rectangle.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>BF_DIAGONAL</dt>
</dl>
</td>
<td width="60%">
Diagonal border.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>BF_DIAGONAL_ENDBOTTOMLEFT</dt>
</dl>
</td>
<td width="60%">
Diagonal border. The end point is the lower-left corner of the rectangle; the origin is the upper-right corner.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>BF_DIAGONAL_ENDBOTTOMRIGHT</dt>
</dl>
</td>
<td width="60%">
Diagonal border. The end point is the lower-right corner of the rectangle; the origin is the upper-left corner.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>BF_DIAGONAL_ENDTOPLEFT</dt>
</dl>
</td>
<td width="60%">
Diagonal border. The end point is the upper-left corner of the rectangle; the origin is the lower-right corner.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>BF_DIAGONAL_ENDTOPRIGHT</dt>
</dl>
</td>
<td width="60%">
Diagonal border. The end point is the upper-right corner of the rectangle; the origin is the lower-left corner.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>BF_FLAT</dt>
</dl>
</td>
<td width="60%">
Flat border.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>BF_LEFT</dt>
</dl>
</td>
<td width="60%">
Left side of border rectangle.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>BF_MIDDLE</dt>
</dl>
</td>
<td width="60%">
Interior of the rectangle is to be filled.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>BF_MONO</dt>
</dl>
</td>
<td width="60%">
One-dimensional border.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>BF_RECT</dt>
</dl>
</td>
<td width="60%">
Entire border rectangle.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>BF_RIGHT</dt>
</dl>
</td>
<td width="60%">
Right side of border rectangle.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>BF_SOFT</dt>
</dl>
</td>
<td width="60%">
Soft buttons instead of tiles.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>BF_TOP</dt>
</dl>
</td>
<td width="60%">
Top of border rectangle.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>BF_TOPLEFT</dt>
</dl>
</td>
<td width="60%">
Top and left side of border rectangle.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>BF_TOPRIGHT</dt>
</dl>
</td>
<td width="60%">
Top and right side of border rectangle.

</td>
</tr>
</table>
 


### -param pContentRect [out]

Type: <b>LPRECT</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that contains, in logical coordinates, the rectangle that receives the interior rectangle, if <i>uFlags</i> is set to BF_ADJUST. This parameter may be set to <b>NULL</b>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b0e22022-fea9-43d1-8ef0-7a1c518760f1">Property Identifiers</a>
 

 

