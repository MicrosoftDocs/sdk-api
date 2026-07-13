---
UID: NF:uxtheme.GetThemeAppProperties
title: GetThemeAppProperties function (uxtheme.h)
description: Retrieves the property flags that control how visual styles are applied in the current application.
helpviewer_keywords: ["GetThemeAppProperties","GetThemeAppProperties function [Windows Controls]","controls.GetThemeAppProperties","controls.inet_GetThemeAppProperties","inet_GetThemeAppProperties","inet_GetThemeAppProperties_cpp","uxtheme/GetThemeAppProperties"]
old-location: controls\GetThemeAppProperties.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemeappproperties.htm
ms.date: 12/05/2018
ms.keywords: GetThemeAppProperties, GetThemeAppProperties function [Windows Controls], controls.GetThemeAppProperties, controls.inet_GetThemeAppProperties, inet_GetThemeAppProperties, inet_GetThemeAppProperties_cpp, uxtheme/GetThemeAppProperties
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
 - GetThemeAppProperties
 - uxtheme/GetThemeAppProperties
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
 - GetThemeAppProperties
---

# GetThemeAppProperties function


## -description

Retrieves the property flags that control how visual styles are applied in the current application.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

The following return values are bit flags combined with a logical OR operator.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STAP_ALLOW_NONCLIENT</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the nonclient areas of application windows have visual styles applied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STAP_ALLOW_CONTROLS</b></dt>
</dl>
</td>
<td width="60%">
Specifies that controls in application windows have visual styles applied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STAP_ALLOW_WEBCONTENT</b></dt>
</dl>
</td>
<td width="60%">
Specifies that all web content displayed in an application is rendered using visual styles.

</td>
</tr>
</table>

## -remarks

Individual flags can be extracted from the result by combining the result with the logical AND of the desired flag.

Do not call this function during <a href="/windows/desktop/Dlls/dllmain">DllMain</a> or global objects constructors. This may cause invalid return values.


#### Examples

The example extracts a single flag's state from the function result.


```cpp
DWORD resultFlags = GetThemeAppProperties();
bool ctrlsAreThemed = ((resultFlags & STAP_ALLOW_CONTROLS) != 0);

```

## -see-also

<a href="/windows/desktop/api/uxtheme/nf-uxtheme-setthemeappproperties">SetThemeAppProperties</a>
