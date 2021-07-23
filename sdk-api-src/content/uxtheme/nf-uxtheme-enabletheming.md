---
UID: NF:uxtheme.EnableTheming
title: EnableTheming function (uxtheme.h)
description: Windows Vista through Windows 7:\_Enables or disables visual styles for the current user in the current and later sessions.Windows 8 and later:\_This function does nothing. Visual styles are always enabled in Windows 8 and later.
helpviewer_keywords: ["EnableTheming","EnableTheming function [Windows Controls]","controls.EnableTheming","controls.inet_EnableTheming","inet_EnableTheming","inet_EnableTheming_cpp","uxtheme/EnableTheming"]
old-location: controls\EnableTheming.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\enabletheming.htm
ms.date: 12/05/2018
ms.keywords: EnableTheming, EnableTheming function [Windows Controls], controls.EnableTheming, controls.inet_EnableTheming, inet_EnableTheming, inet_EnableTheming_cpp, uxtheme/EnableTheming
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
 - EnableTheming
 - uxtheme/EnableTheming
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
 - EnableTheming
---

# EnableTheming function


## -description

<b>Windows Vista through Windows 7</b>: Enables or disables visual styles for the current user in the current and later sessions.

<b>Windows 8 and later</b>: This function does nothing. Visual styles are always enabled in Windows 8 and later.

## -parameters

### -param fEnable [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Receives one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>TRUE</dt>
</dl>
</td>
<td width="60%">
Enables visual styles. If the user previously had an active visual style, it becomes active again.



<div class="alert"><b>Note</b>  Only clients with trusted computing base (TCB) privileges, where the client acts as part of the operating system, can load or change a global theme.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>FALSE</dt>
</dl>
</td>
<td width="60%">
Disables visual styles and turns visual styles off.

</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.