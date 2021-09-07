---
UID: NF:uxtheme.EnableThemeDialogTexture
title: EnableThemeDialogTexture function (uxtheme.h)
description: Enables or disables the visual style of the background of a dialog window.
helpviewer_keywords: ["EnableThemeDialogTexture","EnableThemeDialogTexture function [Windows Controls]","controls.EnableThemeDialogTexture","controls.inet_EnableThemeDialogTexture","inet_EnableThemeDialogTexture","inet_EnableThemeDialogTexture_cpp","uxtheme/EnableThemeDialogTexture"]
old-location: controls\EnableThemeDialogTexture.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\enablethemedialogtexture.htm
ms.date: 12/05/2018
ms.keywords: EnableThemeDialogTexture, EnableThemeDialogTexture function [Windows Controls], controls.EnableThemeDialogTexture, controls.inet_EnableThemeDialogTexture, inet_EnableThemeDialogTexture, inet_EnableThemeDialogTexture_cpp, uxtheme/EnableThemeDialogTexture
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
 - EnableThemeDialogTexture
 - uxtheme/EnableThemeDialogTexture
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
 - EnableThemeDialogTexture
---

# EnableThemeDialogTexture function


## -description

Enables or disables the visual style of the background of a dialog window.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Window handle of the target dialog box.

### -param dwFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

One of the following option flag values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>ETDT_DISABLE</dt>
</dl>
</td>
<td width="60%">
Disables background texturing.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>ETDT_ENABLE</dt>
</dl>
</td>
<td width="60%">
Enables dialog window background texturing. The texturing is defined by a visual style.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>ETDT_USETABTEXTURE</dt>
</dl>
</td>
<td width="60%">
Uses the Tab control texture for the background texture of a dialog window.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>ETDT_USEAEROWIZARDTABTEXTURE</dt>
</dl>
</td>
<td width="60%">
Uses the Aero wizard texture for the background texture of a dialog window.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>ETDT_ENABLETAB</dt>
</dl>
</td>
<td width="60%">
Enables dialog window background texturing. The texture is the Tab control texture defined by the visual style. This flag is equivalent to (ETDT_ENABLE | ETDT_USETABTEXTURE).

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>ETDT_ENABLEAEROWIZARDTAB</dt>
</dl>
</td>
<td width="60%">
ETDT_ENABLE | ETDT_USEAEROWIZARDTABTEXTURE.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>ETDT_VALIDBITS</dt>
</dl>
</td>
<td width="60%">
ETDT_DISABLE | ETDT_ENABLE | ETDT_USETABTEXTURE | ETDT_USEAEROWIZARDTABTEXTURE.

</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>EnableThemeDialogTexture</b> can be used to tailor dialog box compatibility with child windows and controls that may or may not coordinate rendering their client area backgrounds with that of their parent dialog box.