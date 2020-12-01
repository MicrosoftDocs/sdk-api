---
UID: NF:uxtheme.IsThemeDialogTextureEnabled
title: IsThemeDialogTextureEnabled function (uxtheme.h)
description: Reports whether a specified dialog window supports background texturing.
helpviewer_keywords: ["IsThemeDialogTextureEnabled","IsThemeDialogTextureEnabled function [Windows Controls]","controls.IsThemeDialogTextureEnabled","controls.inet_IsThemeDialogTextureEnabled","inet_IsThemeDialogTextureEnabled","inet_IsThemeDialogTextureEnabled_cpp","uxtheme/IsThemeDialogTextureEnabled"]
old-location: controls\IsThemeDialogTextureEnabled.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\isthemedialogtextureenabled.htm
ms.date: 12/05/2018
ms.keywords: IsThemeDialogTextureEnabled, IsThemeDialogTextureEnabled function [Windows Controls], controls.IsThemeDialogTextureEnabled, controls.inet_IsThemeDialogTextureEnabled, inet_IsThemeDialogTextureEnabled, inet_IsThemeDialogTextureEnabled_cpp, uxtheme/IsThemeDialogTextureEnabled
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
 - IsThemeDialogTextureEnabled
 - uxtheme/IsThemeDialogTextureEnabled
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
 - IsThemeDialogTextureEnabled
---

# IsThemeDialogTextureEnabled function


## -description

Reports whether a specified dialog window supports background texturing.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

<b>HWND</b> value that specifies a dialog window.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
Background texturing is supported on the dialog window specified by the <i>hwnd</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Background texturing is not supported on the dialog window specified by the <i>hwnd</i> parameter.

</td>
</tr>
</table>