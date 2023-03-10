---
UID: NF:uxtheme.GetThemeSysSize
title: GetThemeSysSize function (uxtheme.h)
description: Retrieves the value of a system size metric from theme data.
helpviewer_keywords: ["GetThemeSysSize","GetThemeSysSize function [Windows Controls]","SM_CXBORDER","SM_CXHSCROLL","SM_CXMENUSIZE","SM_CXPADDEDBORDER","SM_CXSIZE","SM_CXSMSIZE","SM_CXVSCROLL","SM_CYMENUSIZE","SM_CYSIZE","SM_CYSMSIZE","controls.GetThemeSysSize","controls.inet_GetThemeSysSize","inet_GetThemeSysSize","inet_GetThemeSysSize_cpp","uxtheme/GetThemeSysSize"]
old-location: controls\GetThemeSysSize.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemesyssize.htm
ms.date: 12/05/2018
ms.keywords: GetThemeSysSize, GetThemeSysSize function [Windows Controls], SM_CXBORDER, SM_CXHSCROLL, SM_CXMENUSIZE, SM_CXPADDEDBORDER, SM_CXSIZE, SM_CXSMSIZE, SM_CXVSCROLL, SM_CYMENUSIZE, SM_CYSIZE, SM_CYSMSIZE, controls.GetThemeSysSize, controls.inet_GetThemeSysSize, inet_GetThemeSysSize, inet_GetThemeSysSize_cpp, uxtheme/GetThemeSysSize
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
 - GetThemeSysSize
 - uxtheme/GetThemeSysSize
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
 - GetThemeSysSize
---

# GetThemeSysSize function


## -description

Retrieves the value of a system size metric from theme data.

## -parameters

### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to theme data.

### -param iSizeId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the system size metric desired. The following values are valid:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SM_CXBORDER"></a><a id="sm_cxborder"></a><dl>
<dt><b>SM_CXBORDER</b></dt>
</dl>
</td>
<td width="60%">
Specifies the width of a border.

</td>
</tr>
<tr>
<td width="40%"><a id="SM_CXVSCROLL"></a><a id="sm_cxvscroll"></a><dl>
<dt><b>SM_CXVSCROLL</b></dt>
</dl>
</td>
<td width="60%">
Specifies the width of a scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="SM_CXHSCROLL"></a><a id="sm_cxhscroll"></a><dl>
<dt><b>SM_CXHSCROLL</b></dt>
</dl>
</td>
<td width="60%">
Specifies the height of a scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="SM_CXSIZE"></a><a id="sm_cxsize"></a><dl>
<dt><b>SM_CXSIZE</b></dt>
</dl>
</td>
<td width="60%">
Specifies the width of a caption.

</td>
</tr>
<tr>
<td width="40%"><a id="SM_CYSIZE"></a><a id="sm_cysize"></a><dl>
<dt><b>SM_CYSIZE</b></dt>
</dl>
</td>
<td width="60%">
Specifies the height of a caption.

</td>
</tr>
<tr>
<td width="40%"><a id="SM_CXSMSIZE"></a><a id="sm_cxsmsize"></a><dl>
<dt><b>SM_CXSMSIZE</b></dt>
</dl>
</td>
<td width="60%">
Specifies the width of a small caption.

</td>
</tr>
<tr>
<td width="40%"><a id="SM_CYSMSIZE"></a><a id="sm_cysmsize"></a><dl>
<dt><b>SM_CYSMSIZE</b></dt>
</dl>
</td>
<td width="60%">
Specifies the height of a small caption.

</td>
</tr>
<tr>
<td width="40%"><a id="SM_CXMENUSIZE"></a><a id="sm_cxmenusize"></a><dl>
<dt><b>SM_CXMENUSIZE</b></dt>
</dl>
</td>
<td width="60%">
Specifies the width of a menu bar.

</td>
</tr>
<tr>
<td width="40%"><a id="SM_CYMENUSIZE"></a><a id="sm_cymenusize"></a><dl>
<dt><b>SM_CYMENUSIZE</b></dt>
</dl>
</td>
<td width="60%">
Specifies the height of a menu bar.

</td>
</tr>
<tr>
<td width="40%"><a id="SM_CXPADDEDBORDER"></a><a id="sm_cxpaddedborder"></a><dl>
<dt><b>SM_CXPADDEDBORDER</b></dt>
</dl>
</td>
<td width="60%">
Specifies the amount of border padding for captioned windows.

</td>
</tr>
</table>

## -returns

Type: <b>int</b>

Returns the size in pixels.

## -remarks

 If <i>hTheme</i> is <b> not </b>  <b>NULL</b>, this function returns the size stored in the current visual style (SysMetrics section of the visual style) scaled to the current screen dpi.  If <i>hTheme</i> is <b>NULL</b>, this function returns the global system metric in pixels that is scaled to the current dpi only if the application is marked as dpi-aware; otherwise, the pixels returned are unscaled.

