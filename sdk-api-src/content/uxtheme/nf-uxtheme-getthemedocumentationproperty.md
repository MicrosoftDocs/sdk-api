---
UID: NF:uxtheme.GetThemeDocumentationProperty
title: GetThemeDocumentationProperty function (uxtheme.h)
description: Retrieves the value for a theme property from the documentation section of the specified theme file.
helpviewer_keywords: ["GetThemeDocumentationProperty","GetThemeDocumentationProperty function [Windows Controls]","SZ_THDOCPROP_AUTHOR","SZ_THDOCPROP_CANONICALNAME","SZ_THDOCPROP_DISPLAYNAME","SZ_THDOCPROP_TOOLTIP","controls.GetThemeDocumentationProperty","controls.inet_GetThemeDocumentationProperty","inet_GetThemeDocumentationProperty","inet_GetThemeDocumentationProperty_cpp","uxtheme/GetThemeDocumentationProperty"]
old-location: controls\GetThemeDocumentationProperty.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemedocumentationproperty.htm
ms.date: 12/05/2018
ms.keywords: GetThemeDocumentationProperty, GetThemeDocumentationProperty function [Windows Controls], SZ_THDOCPROP_AUTHOR, SZ_THDOCPROP_CANONICALNAME, SZ_THDOCPROP_DISPLAYNAME, SZ_THDOCPROP_TOOLTIP, controls.GetThemeDocumentationProperty, controls.inet_GetThemeDocumentationProperty, inet_GetThemeDocumentationProperty, inet_GetThemeDocumentationProperty_cpp, uxtheme/GetThemeDocumentationProperty
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
 - GetThemeDocumentationProperty
 - uxtheme/GetThemeDocumentationProperty
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
 - GetThemeDocumentationProperty
---

# GetThemeDocumentationProperty function


## -description

Retrieves the value for a theme property from the documentation section of the specified theme file.

## -parameters

### -param pszThemeName [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

Pointer to a string that contains the name of the theme file that will be opened to query for the property.

### -param pszPropertyName [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

Pointer to a string that contains the name of the theme property to query. Can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SZ_THDOCPROP_DISPLAYNAME"></a><a id="sz_thdocprop_displayname"></a><dl>
<dt><b>SZ_THDOCPROP_DISPLAYNAME</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the display name of the theme. 

</td>
</tr>
<tr>
<td width="40%"><a id="SZ_THDOCPROP_TOOLTIP"></a><a id="sz_thdocprop_tooltip"></a><dl>
<dt><b>SZ_THDOCPROP_TOOLTIP</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the tooltip associated with this theme.

</td>
</tr>
<tr>
<td width="40%"><a id="SZ_THDOCPROP_AUTHOR"></a><a id="sz_thdocprop_author"></a><dl>
<dt><b>SZ_THDOCPROP_AUTHOR</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the name of the author of the theme.

</td>
</tr>
<tr>
<td width="40%"><a id="SZ_THDOCPROP_CANONICALNAME"></a><a id="sz_thdocprop_canonicalname"></a><dl>
<dt><b>SZ_THDOCPROP_CANONICALNAME</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the name of the theme.

</td>
</tr>
</table>

### -param pszValueBuff [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPWSTR</a></b>

Pointer to a string buffer that receives the property string value.

### -param cchMaxValChars [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the maximum number of characters that <i>pszValueBuff</i> can contain.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the theme property has been localized in the theme files string table, this function returns the localized version.