---
UID: NF:uxtheme.GetThemeBool
title: GetThemeBool function (uxtheme.h)
description: Retrieves the value of a BOOL property from the SysMetrics section of theme data.
helpviewer_keywords: ["GetThemeBool","GetThemeBool function [Windows Controls]","TMT_ALWAYSSHOWSIZINGBAR","TMT_AUTOSIZE","TMT_BGFILL","TMT_BORDERONLY","TMT_COMPOSITED","TMT_GLYPHONLY","TMT_GLYPHTRANSPARENT","TMT_INTEGRALSIZING","TMT_MIRRORIMAGE","TMT_SOURCEGROW","TMT_SOURCESHRINK","TMT_TRANSPARENT","TMT_UNIFORMSIZING","TMT_USERPICTURE","controls.GetThemeBool","controls.inet_GetThemeBool","inet_GetThemeBool","inet_GetThemeBool_cpp","uxtheme/GetThemeBool"]
old-location: controls\GetThemeBool.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemebool.htm
ms.date: 12/05/2018
ms.keywords: GetThemeBool, GetThemeBool function [Windows Controls], TMT_ALWAYSSHOWSIZINGBAR, TMT_AUTOSIZE, TMT_BGFILL, TMT_BORDERONLY, TMT_COMPOSITED, TMT_GLYPHONLY, TMT_GLYPHTRANSPARENT, TMT_INTEGRALSIZING, TMT_MIRRORIMAGE, TMT_SOURCEGROW, TMT_SOURCESHRINK, TMT_TRANSPARENT, TMT_UNIFORMSIZING, TMT_USERPICTURE, controls.GetThemeBool, controls.inet_GetThemeBool, inet_GetThemeBool, inet_GetThemeBool_cpp, uxtheme/GetThemeBool
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
req.lib: UxTheme.lib
req.dll: UxTheme.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetThemeBool
 - uxtheme/GetThemeBool
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - UxTheme.dll
api_name:
 - GetThemeBool
---

# GetThemeBool function


## -description

Retrieves the value of a <b>BOOL</b> property from the SysMetrics section of theme data.

## -parameters

### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata">OpenThemeData</a> to create an HTHEME.

### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part containing the BOOL property. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param iPropId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the property to retrieve. May be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TMT_TRANSPARENT"></a><a id="tmt_transparent"></a><dl>
<dt><b>TMT_TRANSPARENT</b></dt>
</dl>
</td>
<td width="60%">
<b>TRUE</b> if the image associated with the part and state have transparent areas. See <a href="/windows/desktop/api/uxtheme/nf-uxtheme-getthemecolor">GetThemeColor</a> for the definition of the TMT_TRANSPARENTCOLOR value that defines the transparent color.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_AUTOSIZE"></a><a id="tmt_autosize"></a><dl>
<dt><b>TMT_AUTOSIZE</b></dt>
</dl>
</td>
<td width="60%">
<b>TRUE</b> if the nonclient caption area associated with the part and state vary with text width.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_BORDERONLY"></a><a id="tmt_borderonly"></a><dl>
<dt><b>TMT_BORDERONLY</b></dt>
</dl>
</td>
<td width="60%">
<b>TRUE</b> if the image associated with the part and state should only have its border drawn.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_COMPOSITED"></a><a id="tmt_composited"></a><dl>
<dt><b>TMT_COMPOSITED</b></dt>
</dl>
</td>
<td width="60%">
<b>TRUE</b> if the control associated with the part and state will handle its own compositing of images.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_BGFILL"></a><a id="tmt_bgfill"></a><dl>
<dt><b>TMT_BGFILL</b></dt>
</dl>
</td>
<td width="60%">
<b>TRUE</b> if true-sized images associated with this part and state are to be drawn on the background fill.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_GLYPHTRANSPARENT"></a><a id="tmt_glyphtransparent"></a><dl>
<dt><b>TMT_GLYPHTRANSPARENT</b></dt>
</dl>
</td>
<td width="60%">
<b>TRUE</b> if the glyph associated with this part and state have transparent areas. See <a href="/windows/desktop/api/uxtheme/nf-uxtheme-getthemecolor">GetThemeColor</a> for the definition of the TMT_GLYPHCOLOR value that defines the transparent color.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_GLYPHONLY"></a><a id="tmt_glyphonly"></a><dl>
<dt><b>TMT_GLYPHONLY</b></dt>
</dl>
</td>
<td width="60%">
<b>TRUE</b> if the glyph associated with this part and state should be drawn without a background.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_ALWAYSSHOWSIZINGBAR"></a><a id="tmt_alwaysshowsizingbar"></a><dl>
<dt><b>TMT_ALWAYSSHOWSIZINGBAR</b></dt>
</dl>
</td>
<td width="60%">
<b>TRUE</b> if the sizing bar associated with this part and state should always be shown.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_MIRRORIMAGE"></a><a id="tmt_mirrorimage"></a><dl>
<dt><b>TMT_MIRRORIMAGE</b></dt>
</dl>
</td>
<td width="60%">
<b>TRUE</b> if the image associated with this part and state should be flipped if the window is being viewed in right-to-left reading mode.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_UNIFORMSIZING"></a><a id="tmt_uniformsizing"></a><dl>
<dt><b>TMT_UNIFORMSIZING</b></dt>
</dl>
</td>
<td width="60%">
<b>TRUE</b> if the image associated with this part and state must have equal height and width.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_INTEGRALSIZING"></a><a id="tmt_integralsizing"></a><dl>
<dt><b>TMT_INTEGRALSIZING</b></dt>
</dl>
</td>
<td width="60%">
<b>TRUE</b> if the truesize image or border associated with this part and state must be sized to a factor of 2.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_SOURCEGROW"></a><a id="tmt_sourcegrow"></a><dl>
<dt><b>TMT_SOURCEGROW</b></dt>
</dl>
</td>
<td width="60%">
<b>TRUE</b> if the image associated with this part and state will scale larger in size if necessary.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_SOURCESHRINK"></a><a id="tmt_sourceshrink"></a><dl>
<dt><b>TMT_SOURCESHRINK</b></dt>
</dl>
</td>
<td width="60%">
<b>TRUE</b> if the image associated with this part and state will scale smaller in size if necessary.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_USERPICTURE"></a><a id="tmt_userpicture"></a><dl>
<dt><b>TMT_USERPICTURE</b></dt>
</dl>
</td>
<td width="60%">
<b>TRUE</b> if the image associated with this part and state is based on the current user.

</td>
</tr>
</table>

### -param pfVal [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a>*</b>

Pointer to a <b>BOOL</b> that receives the retrieved property value.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/Controls/property-typedefs">Property Identifiers</a>