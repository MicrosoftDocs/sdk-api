---
UID: NF:uxtheme.IsThemePartDefined
title: IsThemePartDefined function (uxtheme.h)
description: Retrieves whether a visual style has defined parameters for the specified part and state.
helpviewer_keywords: ["IsThemePartDefined","IsThemePartDefined function [Windows Controls]","controls.IsThemePartDefined","controls.inet_IsThemePartDefined","inet_IsThemePartDefined","inet_IsThemePartDefined_cpp","uxtheme/IsThemePartDefined"]
old-location: controls\IsThemePartDefined.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\isthemepartdefined.htm
ms.date: 12/05/2018
ms.keywords: IsThemePartDefined, IsThemePartDefined function [Windows Controls], controls.IsThemePartDefined, controls.inet_IsThemePartDefined, inet_IsThemePartDefined, inet_IsThemePartDefined_cpp, uxtheme/IsThemePartDefined
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
 - IsThemePartDefined
 - uxtheme/IsThemePartDefined
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
 - IsThemePartDefined
---

# IsThemePartDefined function


## -description

Retrieves whether a visual style has defined parameters for the specified part and state.

## -parameters

### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata">OpenThemeData</a> to create an HTHEME.

### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param iStateId [in]

Type: <b>int</b>

Currently unused. The value should be 0.

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
The theme has defined parameters for the specified <i>iPartId</i> and <i>iStateId</i>

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The theme does not have defined parameters for the specified <i>iPartId</i> and <i>iStateId</i>

</td>
</tr>
</table>