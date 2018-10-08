---
UID: NS:uxtheme._DTTOPTS
title: "_DTTOPTS"
author: windows-sdk-content
description: Defines the options for the DrawThemeTextEx function.
old-location: controls\DTTOPTS.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\userex\structures\dttopts.htm
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: "*PDTTOPTS, DTTOPTS, DTTOPTS structure [Windows Controls], DTT_APPLYOVERLAY, DTT_BORDERCOLOR, DTT_BORDERSIZE, DTT_CALCRECT, DTT_CALLBACK, DTT_COLORPROP, DTT_COMPOSITED, DTT_FONTPROP, DTT_GLOWSIZE, DTT_SHADOWCOLOR, DTT_SHADOWOFFSET, DTT_SHADOWTYPE, DTT_STATEID, DTT_TEXTCOLOR, DTT_VALIDBITS, PDTTOPTS, PDTTOPTS structure pointer [Windows Controls], TST_CONTINUOUS, TST_NONE, TST_SINGLE, _DTTOPTS, controls.DTTOPTS, controls.inet_DTTOPTS, inet_DTTOPTS, inet_DTTOPTS_cpp, uxtheme/DTTOPTS, uxtheme/PDTTOPTS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Uxtheme.h
api_name:
 - DTTOPTS
product: Windows
targetos: Windows
req.typenames: DTTOPTS, *PDTTOPTS
req.redist: 
---

# _DTTOPTS structure


## -description


Defines the options for the <a href="https://msdn.microsoft.com/en-us/library/Bb773317(v=VS.85).aspx">DrawThemeTextEx</a> function.


## -struct-fields




### -field dwSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Size of the structure.


### -field dwFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

A combination of flags that specify whether certain values of the <b>DTTOPTS</b> structure have been specified, and how to interpret these values. This member can be a combination of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DTT_TEXTCOLOR"></a><a id="dtt_textcolor"></a><dl>
<dt><b>DTT_TEXTCOLOR</b></dt>
</dl>
</td>
<td width="60%">
The <b>crText</b> member value is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="DTT_BORDERCOLOR"></a><a id="dtt_bordercolor"></a><dl>
<dt><b>DTT_BORDERCOLOR</b></dt>
</dl>
</td>
<td width="60%">
The <b>crBorder</b> member value is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="DTT_SHADOWCOLOR"></a><a id="dtt_shadowcolor"></a><dl>
<dt><b>DTT_SHADOWCOLOR</b></dt>
</dl>
</td>
<td width="60%">
The <b>crShadow</b> member value is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="DTT_SHADOWTYPE"></a><a id="dtt_shadowtype"></a><dl>
<dt><b>DTT_SHADOWTYPE</b></dt>
</dl>
</td>
<td width="60%">
The <b>iTextShadowType</b> member value is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="DTT_SHADOWOFFSET"></a><a id="dtt_shadowoffset"></a><dl>
<dt><b>DTT_SHADOWOFFSET</b></dt>
</dl>
</td>
<td width="60%">
The <b>ptShadowOffset</b> member value is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="DTT_BORDERSIZE"></a><a id="dtt_bordersize"></a><dl>
<dt><b>DTT_BORDERSIZE</b></dt>
</dl>
</td>
<td width="60%">
The <b>iBorderSize</b> member value is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="DTT_FONTPROP"></a><a id="dtt_fontprop"></a><dl>
<dt><b>DTT_FONTPROP</b></dt>
</dl>
</td>
<td width="60%">
The <b>iFontPropId</b> member value is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="DTT_COLORPROP"></a><a id="dtt_colorprop"></a><dl>
<dt><b>DTT_COLORPROP</b></dt>
</dl>
</td>
<td width="60%">
The <b>iColorPropId</b> member value is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="DTT_STATEID"></a><a id="dtt_stateid"></a><dl>
<dt><b>DTT_STATEID</b></dt>
</dl>
</td>
<td width="60%">
The <b>iStateId</b> member value is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="DTT_CALCRECT"></a><a id="dtt_calcrect"></a><dl>
<dt><b>DTT_CALCRECT</b></dt>
</dl>
</td>
<td width="60%">
The <i>pRect</i> parameter of the <a href="https://msdn.microsoft.com/en-us/library/Bb773317(v=VS.85).aspx">DrawThemeTextEx</a> function that uses this structure will be used as both an in and an out parameter. After the function returns, the <i>pRect</i> parameter will contain the rectangle that corresponds to the region calculated to be drawn.

</td>
</tr>
<tr>
<td width="40%"><a id="DTT_APPLYOVERLAY"></a><a id="dtt_applyoverlay"></a><dl>
<dt><b>DTT_APPLYOVERLAY</b></dt>
</dl>
</td>
<td width="60%">
The <b>fApplyOverlay</b> member value is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="DTT_GLOWSIZE"></a><a id="dtt_glowsize"></a><dl>
<dt><b>DTT_GLOWSIZE</b></dt>
</dl>
</td>
<td width="60%">
The <b>iGlowSize</b> member value is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="DTT_CALLBACK"></a><a id="dtt_callback"></a><dl>
<dt><b>DTT_CALLBACK</b></dt>
</dl>
</td>
<td width="60%">
The <b>pfnDrawTextCallback</b> member value is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="DTT_COMPOSITED"></a><a id="dtt_composited"></a><dl>
<dt><b>DTT_COMPOSITED</b></dt>
</dl>
</td>
<td width="60%">
Draws text with antialiased alpha. Use of this flag requires a top-down DIB section. This flag works only if the HDC passed to function <a href="https://msdn.microsoft.com/en-us/library/Bb773317(v=VS.85).aspx">DrawThemeTextEx</a> has a top-down DIB section currently selected in it. For more information, see <a href="https://msdn.microsoft.com/56b39a3d-48a4-4620-9652-ec41ea4d6423">Device-Independent Bitmaps</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="DTT_VALIDBITS"></a><a id="dtt_validbits"></a><dl>
<dt><b>DTT_VALIDBITS</b></dt>
</dl>
</td>
<td width="60%">
DTT_TEXTCOLOR |  DTT_BORDERCOLOR | DTT_SHADOWCOLOR | DTT_SHADOWTYPE | 
              DTT_SHADOWOFFSET | DTT_BORDERSIZE | DTT_FONTPROP | DTT_COLORPROP | DTT_STATEID | DTT_CALCRECT |  DTT_APPLYOVERLAY | DTT_GLOWSIZE | DTT_COMPOSITED.

</td>
</tr>
</table>
 


### -field crText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

Specifies the color of the text that will be drawn.


### -field crBorder

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

Specifies the color of the outline that will be drawn around the text.


### -field crShadow

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

Specifies the color of the shadow that will be drawn behind the text.


### -field iTextShadowType

Type: <b>int</b>

Specifies the type of the shadow that will be drawn behind the text. This member can have one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TST_NONE"></a><a id="tst_none"></a><dl>
<dt><b>TST_NONE</b></dt>
</dl>
</td>
<td width="60%">
No shadow will be drawn.

</td>
</tr>
<tr>
<td width="40%"><a id="TST_SINGLE"></a><a id="tst_single"></a><dl>
<dt><b>TST_SINGLE</b></dt>
</dl>
</td>
<td width="60%">
The shadow will be drawn to appear detailed underneath text.

</td>
</tr>
<tr>
<td width="40%"><a id="TST_CONTINUOUS"></a><a id="tst_continuous"></a><dl>
<dt><b>TST_CONTINUOUS</b></dt>
</dl>
</td>
<td width="60%">
The shadow will be drawn to appear blurred underneath text.

</td>
</tr>
</table>
 


### -field ptShadowOffset

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a></b>

Specifies the amount of offset, in logical coordinates, between the shadow and the text.


### -field iBorderSize

Type: <b>int</b>

Specifies the radius of the outline that will be drawn around the text.


### -field iFontPropId

Type: <b>int</b>

Specifies an alternate font property to use when drawing text. For a list of possible values, see <a href="https://msdn.microsoft.com/en-us/library/Bb759783(v=VS.85).aspx">GetThemeSysFont</a>.


### -field iColorPropId

Type: <b>int</b>

Specifies an alternate color property to use when drawing text. If this value is valid and the corresponding flag is set in <b>dwFlags</b>, this value will override the value of <b>crText</b>. See the values listed in <a href="https://msdn.microsoft.com/165c1781-161e-4ab2-98c9-eec4e9098d09">GetSysColor</a> for the <i>nIndex</i> parameter.


### -field iStateId

Type: <b>int</b>

Specifies an alternate state to use. This member is not used by <a href="https://msdn.microsoft.com/en-us/library/Bb773317(v=VS.85).aspx">DrawThemeTextEx</a>.


### -field fApplyOverlay

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

If <b>TRUE</b>, text will be drawn on top of the shadow and outline effects. If <b>FALSE</b>, just the shadow and outline effects will be drawn.


### -field iGlowSize

Type: <b>int</b>

Specifies the size of a glow that will be drawn on the background prior to any text being drawn.


### -field pfnDrawTextCallback

Type: <b>DTT_CALLBACK_PROC</b>

Pointer to callback function for <a href="https://msdn.microsoft.com/en-us/library/Bb773317(v=VS.85).aspx">DrawThemeTextEx</a>.


### -field lParam

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

Parameter for callback back function specified by <b>pfnDrawTextCallback</b>.

