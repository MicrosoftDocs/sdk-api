---
UID: NF:uxtheme.SetThemeAppProperties
title: SetThemeAppProperties function (uxtheme.h)
description: Sets the flags that determine how visual styles are implemented in the calling application.
helpviewer_keywords: ["SetThemeAppProperties","SetThemeAppProperties function [Windows Controls]","controls.SetThemeAppProperties","controls.inet_SetThemeAppProperties","inet_SetThemeAppProperties","inet_SetThemeAppProperties_cpp","uxtheme/SetThemeAppProperties"]
old-location: controls\SetThemeAppProperties.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\setthemeappproperties.htm
ms.date: 12/05/2018
ms.keywords: SetThemeAppProperties, SetThemeAppProperties function [Windows Controls], controls.SetThemeAppProperties, controls.inet_SetThemeAppProperties, inet_SetThemeAppProperties, inet_SetThemeAppProperties_cpp, uxtheme/SetThemeAppProperties
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
req.dll: UxTheme.dll (version 1.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetThemeAppProperties
 - uxtheme/SetThemeAppProperties
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
 - SetThemeAppProperties
---

# SetThemeAppProperties function


## -description

Sets the flags that determine how visual styles are implemented in the calling application.

## -parameters

### -param dwFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

<b>DWORD</b> that specifies one or more of the following bit flags, which can be combined with a logical OR.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>STAP_ALLOW_NONCLIENT</dt>
</dl>
</td>
<td width="60%">
Specifies that the nonclient areas of application windows will have visual styles applied.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>STAP_ALLOW_CONTROLS</dt>
</dl>
</td>
<td width="60%">
Specifies that the common controls used in an application will have visual styles applied.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>STAP_ALLOW_WEBCONTENT</dt>
</dl>
</td>
<td width="60%">
Specifies that web content displayed in an application will have visual styles applied.

</td>
</tr>
</table>

## -remarks

After you set the flags, send a <a href="/windows/desktop/winmsg/wm-themechanged">WM_THEMECHANGED</a> message to your application's main window for the changes to take effect. 



#### Examples

This example combines flags and calls this function as shown.


```cpp
DWORD dwFlags = (STAP_ALLOW_NONCLIENT | 
        STAP_ALLOW_CONTROLS | STAP_ALLOW_WEBCONTENT);
SetThemeAppProperties(dwFlags);

```

## -see-also

<a href="/windows/desktop/api/uxtheme/nf-uxtheme-getthemeappproperties">GetThemeAppProperties</a>