---
UID: NF:uxtheme.SetWindowThemeAttribute
title: SetWindowThemeAttribute function (uxtheme.h)
description: Sets attributes to control how visual styles are applied to a specified window.
helpviewer_keywords: ["SetWindowThemeAttribute","SetWindowThemeAttribute function [Windows Controls]","WTA_NONCLIENT","controls.SetWindowThemeAttribute","controls.inet_SetWindowThemeAttribute","inet_SetWindowThemeAttribute","inet_SetWindowThemeAttribute_cpp","uxtheme/SetWindowThemeAttribute"]
old-location: controls\SetWindowThemeAttribute.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\setwindowthemeattribute.htm
ms.date: 12/05/2018
ms.keywords: SetWindowThemeAttribute, SetWindowThemeAttribute function [Windows Controls], WTA_NONCLIENT, controls.SetWindowThemeAttribute, controls.inet_SetWindowThemeAttribute, inet_SetWindowThemeAttribute, inet_SetWindowThemeAttribute_cpp, uxtheme/SetWindowThemeAttribute
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
 - SetWindowThemeAttribute
 - uxtheme/SetWindowThemeAttribute
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
 - SetWindowThemeAttribute
---

# SetWindowThemeAttribute function


## -description

Sets attributes to control how visual styles are applied to a specified window.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a window to apply changes to.

### -param eAttribute [in]

Type: <b>enum WINDOWTHEMEATTRIBUTETYPE</b>

Value of type <a href="/windows/desktop/api/uxtheme/ne-uxtheme-windowthemeattributetype">WINDOWTHEMEATTRIBUTETYPE</a> that specifies the type of attribute to set. The value of this parameter determines the type of data that should be passed in the <i>pvAttribute</i> parameter. Can be the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WTA_NONCLIENT"></a><a id="wta_nonclient"></a><dl>
<dt><b>WTA_NONCLIENT</b></dt>
</dl>
</td>
<td width="60%">
Specifies non-client related attributes. <i>pvAttribute</i> must be a pointer of type <a href="/windows/desktop/api/uxtheme/ns-uxtheme-wta_options">WTA_OPTIONS</a>.
</td>
</tr>
</table>

### -param pvAttribute [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">PVOID</a></b>

A pointer that specifies attributes to set. Type is determined by the value of the <i>eAttribute</i> value.

### -param cbAttribute [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Specifies the size, in bytes, of the data pointed to by <i>pvAttribute</i>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uxtheme/ne-uxtheme-windowthemeattributetype">WINDOWTHEMEATTRIBUTETYPE</a>
