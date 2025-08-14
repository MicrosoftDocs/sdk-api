---
UID: NF:uxtheme.GetThemeMetric
title: GetThemeMetric function (uxtheme.h)
description: Retrieves the value of a metric property.
helpviewer_keywords: ["GetThemeMetric","GetThemeMetric function [Windows Controls]","TMT_ALPHALEVEL","TMT_ALPHATHRESHOLD","TMT_BORDERSIZE","TMT_GLYPHINDEX","TMT_GRADIENTRATIO1","TMT_GRADIENTRATIO2","TMT_GRADIENTRATIO3","TMT_GRADIENTRATIO4","TMT_GRADIENTRATIO5","TMT_HEIGHT","TMT_IMAGECOUNT","TMT_MINDPI1","TMT_MINDPI2","TMT_MINDPI3","TMT_MINDPI4","TMT_MINDPI5","TMT_PROGRESSCHUNKSIZE","TMT_PROGRESSSPACESIZE","TMT_ROUNDCORNERHEIGHT","TMT_ROUNDCORNERWIDTH","TMT_SATURATION","TMT_TEXTBORDERSIZE","TMT_TRUESIZESTRETCHMARK","TMT_WIDTH","controls.GetThemeMetric","controls.inet_GetThemeMetric","inet_GetThemeMetric","inet_GetThemeMetric_cpp","uxtheme/GetThemeMetric"]
old-location: controls\GetThemeMetric.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthememetric.htm
ms.date: 12/05/2018
ms.keywords: GetThemeMetric, GetThemeMetric function [Windows Controls], TMT_ALPHALEVEL, TMT_ALPHATHRESHOLD, TMT_BORDERSIZE, TMT_GLYPHINDEX, TMT_GRADIENTRATIO1, TMT_GRADIENTRATIO2, TMT_GRADIENTRATIO3, TMT_GRADIENTRATIO4, TMT_GRADIENTRATIO5, TMT_HEIGHT, TMT_IMAGECOUNT, TMT_MINDPI1, TMT_MINDPI2, TMT_MINDPI3, TMT_MINDPI4, TMT_MINDPI5, TMT_PROGRESSCHUNKSIZE, TMT_PROGRESSSPACESIZE, TMT_ROUNDCORNERHEIGHT, TMT_ROUNDCORNERWIDTH, TMT_SATURATION, TMT_TEXTBORDERSIZE, TMT_TRUESIZESTRETCHMARK, TMT_WIDTH, controls.GetThemeMetric, controls.inet_GetThemeMetric, inet_GetThemeMetric, inet_GetThemeMetric_cpp, uxtheme/GetThemeMetric
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
 - GetThemeMetric
 - uxtheme/GetThemeMetric
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
 - ext-ms-win-uxtheme-themes-l1-1-1.dll
 - xamlpalwp.dll
api_name:
 - GetThemeMetric
---

# GetThemeMetric function


## -description

Retrieves the value of a metric property.

## -parameters

### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata">OpenThemeData</a> to create an HTHEME.

### -param hdc [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HDC</a></b>

HDC. This parameter may be set to <b>NULL</b>.

### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part that contains the metric property. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param iPropId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the property to retrieve. Can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TMT_ALPHALEVEL"></a><a id="tmt_alphalevel"></a><dl>
<dt><b>TMT_ALPHALEVEL</b></dt>
</dl>
</td>
<td width="60%">
The alpha value (0-255) used for <a href="/windows/desktop/api/uxtheme/nf-uxtheme-drawthemeicon">DrawThemeIcon</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_ALPHATHRESHOLD"></a><a id="tmt_alphathreshold"></a><dl>
<dt><b>TMT_ALPHATHRESHOLD</b></dt>
</dl>
</td>
<td width="60%">
The minimum alpha value (0-255) that a pixel must be to be considered opaque.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_BORDERSIZE"></a><a id="tmt_bordersize"></a><dl>
<dt><b>TMT_BORDERSIZE</b></dt>
</dl>
</td>
<td width="60%">
The thickness of the border drawn if this part uses a border fill.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_GLYPHINDEX"></a><a id="tmt_glyphindex"></a><dl>
<dt><b>TMT_GLYPHINDEX</b></dt>
</dl>
</td>
<td width="60%">
The character index into the selected font that will be used for the glyph, if the part uses a font-based glyph.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_GRADIENTRATIO1"></a><a id="tmt_gradientratio1"></a><dl>
<dt><b>TMT_GRADIENTRATIO1</b></dt>
</dl>
</td>
<td width="60%">
The amount of the first gradient color to use in drawing the part. This value can be from 0 to 255, but this value plus the values of each of the GRADIENTRATIO values must add up to 255. See the TMT_GRADIENTCOLOR1 value of <a href="/windows/desktop/api/uxtheme/nf-uxtheme-getthemecolor">GetThemeColor</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_GRADIENTRATIO2"></a><a id="tmt_gradientratio2"></a><dl>
<dt><b>TMT_GRADIENTRATIO2</b></dt>
</dl>
</td>
<td width="60%">
The amount of the second gradient color to use in drawing the part.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_GRADIENTRATIO3"></a><a id="tmt_gradientratio3"></a><dl>
<dt><b>TMT_GRADIENTRATIO3</b></dt>
</dl>
</td>
<td width="60%">
The amount of the third gradient color to use in drawing the part.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_GRADIENTRATIO4"></a><a id="tmt_gradientratio4"></a><dl>
<dt><b>TMT_GRADIENTRATIO4</b></dt>
</dl>
</td>
<td width="60%">
The amount of the fourth gradient color to use in drawing the part.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_GRADIENTRATIO5"></a><a id="tmt_gradientratio5"></a><dl>
<dt><b>TMT_GRADIENTRATIO5</b></dt>
</dl>
</td>
<td width="60%">
The amount of the fifth gradient color to use in drawing the part.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_HEIGHT"></a><a id="tmt_height"></a><dl>
<dt><b>TMT_HEIGHT</b></dt>
</dl>
</td>
<td width="60%">
The height of the part.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_IMAGECOUNT"></a><a id="tmt_imagecount"></a><dl>
<dt><b>TMT_IMAGECOUNT</b></dt>
</dl>
</td>
<td width="60%">
The number of state images present in an image file.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_MINDPI1"></a><a id="tmt_mindpi1"></a><dl>
<dt><b>TMT_MINDPI1</b></dt>
</dl>
</td>
<td width="60%">
The minimum dpi that the first image file was designed for. See <a href="/windows/desktop/api/uxtheme/nf-uxtheme-getthemefilename">GetThemeFilename</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_MINDPI2"></a><a id="tmt_mindpi2"></a><dl>
<dt><b>TMT_MINDPI2</b></dt>
</dl>
</td>
<td width="60%">
The minimum dpi that the second image file was designed for.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_MINDPI3"></a><a id="tmt_mindpi3"></a><dl>
<dt><b>TMT_MINDPI3</b></dt>
</dl>
</td>
<td width="60%">
The minimum dpi that the third image file was designed for.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_MINDPI4"></a><a id="tmt_mindpi4"></a><dl>
<dt><b>TMT_MINDPI4</b></dt>
</dl>
</td>
<td width="60%">
The minimum dpi that the fourth image file was designed for.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_MINDPI5"></a><a id="tmt_mindpi5"></a><dl>
<dt><b>TMT_MINDPI5</b></dt>
</dl>
</td>
<td width="60%">
The minimum dpi that the fifth image file was designed for.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_PROGRESSCHUNKSIZE"></a><a id="tmt_progresschunksize"></a><dl>
<dt><b>TMT_PROGRESSCHUNKSIZE</b></dt>
</dl>
</td>
<td width="60%">
The size of the progress control "chunk" shapes that define how far an operation has progressed.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_PROGRESSSPACESIZE"></a><a id="tmt_progressspacesize"></a><dl>
<dt><b>TMT_PROGRESSSPACESIZE</b></dt>
</dl>
</td>
<td width="60%">
The total size of all of the progress control "chunks".

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_ROUNDCORNERWIDTH"></a><a id="tmt_roundcornerwidth"></a><dl>
<dt><b>TMT_ROUNDCORNERWIDTH</b></dt>
</dl>
</td>
<td width="60%">
The roundness (0-100%) of the part's corners.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_ROUNDCORNERHEIGHT"></a><a id="tmt_roundcornerheight"></a><dl>
<dt><b>TMT_ROUNDCORNERHEIGHT</b></dt>
</dl>
</td>
<td width="60%">
The roundness (0-100%) of the part's corners.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_SATURATION"></a><a id="tmt_saturation"></a><dl>
<dt><b>TMT_SATURATION</b></dt>
</dl>
</td>
<td width="60%">
The amount of saturation (0-255) to apply to an icon drawn using <a href="/windows/desktop/api/uxtheme/nf-uxtheme-drawthemeicon">DrawThemeIcon</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_TEXTBORDERSIZE"></a><a id="tmt_textbordersize"></a><dl>
<dt><b>TMT_TEXTBORDERSIZE</b></dt>
</dl>
</td>
<td width="60%">
The thickness of the border drawn around text characters.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_TRUESIZESTRETCHMARK"></a><a id="tmt_truesizestretchmark"></a><dl>
<dt><b>TMT_TRUESIZESTRETCHMARK</b></dt>
</dl>
</td>
<td width="60%">
The percentage of a true-size image's original size at which the image will be stretched.

</td>
</tr>
<tr>
<td width="40%"><a id="TMT_WIDTH"></a><a id="tmt_width"></a><dl>
<dt><b>TMT_WIDTH</b></dt>
</dl>
</td>
<td width="60%">
The width of the part.

</td>
</tr>
</table>

### -param piVal [out]

Type: <b>int*</b>

Pointer to an <b>int</b> that receives the metric property value.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/Controls/property-typedefs">Property Identifiers</a>