---
UID: NS:uxtheme._DTBGOPTS
title: DTBGOPTS (uxtheme.h)
description: Defines the options for the DrawThemeBackgroundEx function.
helpviewer_keywords: ["*PDTBGOPTS","DTBGOPTS","DTBGOPTS structure [Windows Controls]","DTBG_CLIPRECT","DTBG_COMPUTINGREGION","DTBG_DRAWSOLID","DTBG_MIRRORDC","DTBG_NOMIRROR","DTBG_OMITBORDER","DTBG_OMITCONTENT","DTBG_VALIDBITS","PDTBGOPTS","PDTBGOPTS structure pointer [Windows Controls]","controls.DTBGOPTS","controls.inet_DTBGOPTS","inet_DTBGOPTS","inet_DTBGOPTS_cpp","uxtheme/DTBGOPTS","uxtheme/PDTBGOPTS"]
old-location: controls\DTBGOPTS.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\structures\dtbgopts.htm
ms.date: 12/05/2018
ms.keywords: '*PDTBGOPTS, DTBGOPTS, DTBGOPTS structure [Windows Controls], DTBG_CLIPRECT, DTBG_COMPUTINGREGION, DTBG_DRAWSOLID, DTBG_MIRRORDC, DTBG_NOMIRROR, DTBG_OMITBORDER, DTBG_OMITCONTENT, DTBG_VALIDBITS, PDTBGOPTS, PDTBGOPTS structure pointer [Windows Controls], controls.DTBGOPTS, controls.inet_DTBGOPTS, inet_DTBGOPTS, inet_DTBGOPTS_cpp, uxtheme/DTBGOPTS, uxtheme/PDTBGOPTS'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DTBGOPTS, *PDTBGOPTS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DTBGOPTS
 - uxtheme/_DTBGOPTS
 - PDTBGOPTS
 - uxtheme/PDTBGOPTS
 - DTBGOPTS
 - uxtheme/DTBGOPTS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Uxtheme.h
api_name:
 - DTBGOPTS
---

# DTBGOPTS structure


## -description

Defines the options for the <a href="/windows/desktop/api/uxtheme/nf-uxtheme-drawthemebackgroundex">DrawThemeBackgroundEx</a> function.

## -struct-fields

### -field dwSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Size of the structure. Set this to sizeof(DTBGOPTS).

### -field dwFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Flags that specify the selected options. This member can be one of the following:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DTBG_CLIPRECT"></a><a id="dtbg_cliprect"></a><dl>
<dt><b>DTBG_CLIPRECT</b></dt>
</dl>
</td>
<td width="60%">
<b>rcClip</b> specifies the rectangle to which drawing is clipped.

</td>
</tr>
<tr>
<td width="40%"><a id="DTBG_DRAWSOLID"></a><a id="dtbg_drawsolid"></a><dl>
<dt><b>DTBG_DRAWSOLID</b></dt>
</dl>
</td>
<td width="60%">
Deprecated. Draw transparent and alpha images as solid.

</td>
</tr>
<tr>
<td width="40%"><a id="DTBG_OMITBORDER"></a><a id="dtbg_omitborder"></a><dl>
<dt><b>DTBG_OMITBORDER</b></dt>
</dl>
</td>
<td width="60%">
Do not draw the border of the part (currently this value is only supported for bgtype=borderfill).

</td>
</tr>
<tr>
<td width="40%"><a id="DTBG_OMITCONTENT"></a><a id="dtbg_omitcontent"></a><dl>
<dt><b>DTBG_OMITCONTENT</b></dt>
</dl>
</td>
<td width="60%">
Do not draw the content area of the part (currently this value is only supported for bgtype=borderfill).

</td>
</tr>
<tr>
<td width="40%"><a id="DTBG_COMPUTINGREGION"></a><a id="dtbg_computingregion"></a><dl>
<dt><b>DTBG_COMPUTINGREGION</b></dt>
</dl>
</td>
<td width="60%">
Deprecated.

</td>
</tr>
<tr>
<td width="40%"><a id="DTBG_MIRRORDC"></a><a id="dtbg_mirrordc"></a><dl>
<dt><b>DTBG_MIRRORDC</b></dt>
</dl>
</td>
<td width="60%">
Assume the <b>hdc</b> is mirrored and flip images as appropriate (currently this value is only supported for bgtype=imagefile).

</td>
</tr>
<tr>
<td width="40%"><a id="DTBG_NOMIRROR"></a><a id="dtbg_nomirror"></a><dl>
<dt><b>DTBG_NOMIRROR</b></dt>
</dl>
</td>
<td width="60%">
Do not mirror the output; even in right-to-left (RTL) layout.

</td>
</tr>
<tr>
<td width="40%"><a id="DTBG_VALIDBITS"></a><a id="dtbg_validbits"></a><dl>
<dt><b>DTBG_VALIDBITS</b></dt>
</dl>
</td>
<td width="60%">
DTBG_CLIPRECT | DTBG_DRAWSOLID | DTBG_OMITBORDER | DTBG_OMITCONTENT | DTBG_COMPUTINGREGION | DTBG_MIRRORDC | DTBG_NOMIRROR.

</td>
</tr>
</table>

### -field rcClip

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

A <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> that specifies the bounding rectangle of the clip region.

## -see-also

<a href="/windows/desktop/api/uxtheme/nf-uxtheme-drawthemebackgroundex">DrawThemeBackgroundEx</a>