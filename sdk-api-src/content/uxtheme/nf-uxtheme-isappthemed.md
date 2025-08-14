---
UID: NF:uxtheme.IsAppThemed
title: IsAppThemed function (uxtheme.h)
description: Reports whether the current application's user interface displays using visual styles.
helpviewer_keywords: ["IsAppThemed","IsAppThemed function [Windows Controls]","controls.IsAppThemed","controls.inet_IsAppThemed","inet_IsAppThemed","inet_IsAppThemed_cpp","uxtheme/IsAppThemed"]
old-location: controls\IsAppThemed.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\isappthemed.htm
ms.date: 12/05/2018
ms.keywords: IsAppThemed, IsAppThemed function [Windows Controls], controls.IsAppThemed, controls.inet_IsAppThemed, inet_IsAppThemed, inet_IsAppThemed_cpp, uxtheme/IsAppThemed
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
 - IsAppThemed
 - uxtheme/IsAppThemed
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
 - Ext-MS-Win-UXTheme-Themes-l1-1-0.dll
 - xamlpalwp.dll
 - ext-ms-win-uxtheme-themes-l1-1-1.dll
api_name:
 - IsAppThemed
---

# IsAppThemed function


## -description

Reports whether the current application's user interface displays using visual styles.



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
The application has a visual style applied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The application does not have a visual style applied.

</td>
</tr>
</table>

## -remarks

Prior to Windows 8, a visual style can be turned off in Control Panel, so that an application can support visual styles but not have a visual style applied at a given time.

 In Windows 8, it is not possible to turn off visual styles.


Do not call this function during <a href="/windows/desktop/Dlls/dllmain">DllMain</a> or global objects constructors. This may cause invalid return values.
