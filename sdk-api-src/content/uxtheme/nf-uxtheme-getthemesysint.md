---
UID: NF:uxtheme.GetThemeSysInt
title: GetThemeSysInt function (uxtheme.h)
description: Retrieves the value of a system int.
helpviewer_keywords: ["GetThemeSysInt","GetThemeSysInt function [Windows Controls]","TMT_MINCOLORDEPTH","controls.GetThemeSysInt","controls.inet_GetThemeSysInt","inet_GetThemeSysInt","inet_GetThemeSysInt_cpp","uxtheme/GetThemeSysInt"]
old-location: controls\GetThemeSysInt.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemesysint.htm
ms.date: 12/05/2018
ms.keywords: GetThemeSysInt, GetThemeSysInt function [Windows Controls], TMT_MINCOLORDEPTH, controls.GetThemeSysInt, controls.inet_GetThemeSysInt, inet_GetThemeSysInt, inet_GetThemeSysInt_cpp, uxtheme/GetThemeSysInt
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
 - GetThemeSysInt
 - uxtheme/GetThemeSysInt
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
 - GetThemeSysInt
---

# GetThemeSysInt function


## -description

Retrieves the value of a system <b>int</b>.

## -parameters

### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to theme data.

### -param iIntId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the desired system <b>int</b>. May be the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TMT_MINCOLORDEPTH"></a><a id="tmt_mincolordepth"></a><dl>
<dt><b>TMT_MINCOLORDEPTH</b></dt>
</dl>
</td>
<td width="60%">
The minimum color depth, in bits, required to properly view this style.

</td>
</tr>
</table>

### -param piValue [in]

Type: <b>int*</b>

Pointer to an <b>int</b> that receives the system integer value.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.