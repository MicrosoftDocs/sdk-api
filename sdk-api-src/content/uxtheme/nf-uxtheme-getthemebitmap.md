---
UID: NF:uxtheme.GetThemeBitmap
title: GetThemeBitmap function (uxtheme.h)
description: Retrieves the bitmap associated with a particular theme, part, state, and property.
helpviewer_keywords: ["GBF_COPY","GBF_DIRECT","GBF_VALIDBITS","GetThemeBitmap","GetThemeBitmap function [Windows Controls]","TMT_DIBDATA","TMT_GLYPHDIBDATA","TMT_HBITMAP","controls.GetThemeBitmap","controls.inet_GetThemeBitmap","inet_GetThemeBitmap","inet_GetThemeBitmap_cpp","uxtheme/GetThemeBitmap"]
old-location: controls\GetThemeBitmap.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemebitmap.htm
ms.date: 12/05/2018
ms.keywords: GBF_COPY, GBF_DIRECT, GBF_VALIDBITS, GetThemeBitmap, GetThemeBitmap function [Windows Controls], TMT_DIBDATA, TMT_GLYPHDIBDATA, TMT_HBITMAP, controls.GetThemeBitmap, controls.inet_GetThemeBitmap, inet_GetThemeBitmap, inet_GetThemeBitmap_cpp, uxtheme/GetThemeBitmap
req.header: uxtheme.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: UxTheme.lib
req.dll: UxTheme.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetThemeBitmap
 - uxtheme/GetThemeBitmap
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-uxtheme-themes-l1-1-3.dll
 - ext-ms-win-uxtheme-themes-l1-1-2.dll
 - UxTheme.dll
 - Ext-MS-Win-UXTheme-Themes-l1-1-0.dll
 - xamlpalwp.dll
 - ext-ms-win-uxtheme-themes-l1-1-1.dll
api_name:
 - GetThemeBitmap
---

# GetThemeBitmap function


## -description

Retrieves the bitmap associated with a particular theme, part, state, and property.

## -parameters

### -param hTheme [in]

Type: <b>HTHEME</b>

A handle to theme data.

### -param iPartId [in]

Type: <b>int</b>

The part that contains the bitmap. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param iStateId [in]

Type: <b>int</b>

The state of the part.

### -param iPropId [in]

Type: <b>int</b>

The property to retrieve. Pass zero to automatically select the first available bitmap for this part and state, 
                or use one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TMT_DIBDATA"></a><a id="tmt_dibdata"></a><dl>
<dt><b>TMT_DIBDATA</b></dt>
</dl>
</td>
<td width="60%">
The background image.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_GLYPHDIBDATA"></a><a id="tmt_glyphdibdata"></a><dl>
<dt><b>TMT_GLYPHDIBDATA</b></dt>
</dl>
</td>
<td width="60%">
The glyph image drawn on top of the background, if present. 

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_HBITMAP"></a><a id="tmt_hbitmap"></a><dl>
<dt><b>TMT_HBITMAP</b></dt>
</dl>
</td>
<td width="60%">
Not currently supported.

</td>
</tr>
</table>

### -param dwFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">ULONG</a></b>

The flags that specify how the bitmap is to be retrieved. Can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GBF_DIRECT"></a><a id="gbf_direct"></a><dl>
<dt><b>GBF_DIRECT</b></dt>
</dl>
</td>
<td width="60%">
Retrieves a handle to the existing bitmap.

</td>
</tr>
<tr>
<td width="40%"><a id="GBF_COPY"></a><a id="gbf_copy"></a><dl>
<dt><b>GBF_COPY</b></dt>
</dl>
</td>
<td width="60%">
Retrieves a copy of the bitmap.

</td>
</tr>
<tr>
<td width="40%"><a id="GBF_VALIDBITS"></a><a id="gbf_validbits"></a><dl>
<dt><b>GBF_VALIDBITS</b></dt>
</dl>
</td>
<td width="60%">
<b>GBF_DIRECT</b> | <b>GBF_COPY</b>

</td>
</tr>
</table>

### -param phBitmap [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HBITMAP</a>*</b>

A pointer that receives a handle to the requested bitmap.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If <i>dwFlags</i> is set to <b>GBF_COPY</b>, release the bitmap stored in <i>phBitmap</i> when no longer needed by calling <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>.