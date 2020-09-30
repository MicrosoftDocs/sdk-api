---
UID: NF:uxtheme.IsThemeBackgroundPartiallyTransparent
title: IsThemeBackgroundPartiallyTransparent function (uxtheme.h)
description: Retrieves whether the background specified by the visual style has transparent pieces or alpha-blended pieces.
helpviewer_keywords: ["IsThemeBackgroundPartiallyTransparent","IsThemeBackgroundPartiallyTransparent function [Windows Controls]","controls.IsThemeBackgroundPartiallyTransparent","controls.inet_IsThemeBackgroundPartiallyTransparent","inet_IsThemeBackgroundPartiallyTransparent","inet_IsThemeBackgroundPartiallyTransparent_cpp","uxtheme/IsThemeBackgroundPartiallyTransparent"]
old-location: controls\IsThemeBackgroundPartiallyTransparent.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\isthemebackgroundpartiallytransparent.htm
ms.date: 12/05/2018
ms.keywords: IsThemeBackgroundPartiallyTransparent, IsThemeBackgroundPartiallyTransparent function [Windows Controls], controls.IsThemeBackgroundPartiallyTransparent, controls.inet_IsThemeBackgroundPartiallyTransparent, inet_IsThemeBackgroundPartiallyTransparent, inet_IsThemeBackgroundPartiallyTransparent_cpp, uxtheme/IsThemeBackgroundPartiallyTransparent
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
 - IsThemeBackgroundPartiallyTransparent
 - uxtheme/IsThemeBackgroundPartiallyTransparent
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
 - IsThemeBackgroundPartiallyTransparent
---

# IsThemeBackgroundPartiallyTransparent function


## -description

Retrieves whether the background specified by the visual style has transparent pieces or alpha-blended pieces.

## -parameters

### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata">OpenThemeData</a> to create an HTHEME.

### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

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
The theme-specified background for a particular <i>iPartId</i> and <i>iStateId</i> has transparent pieces or alpha-blended pieces.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The theme-specified background for a particular <i>iPartId</i> and <i>iStateId</i> does not have transparent pieces or alpha-blended pieces.

</td>
</tr>
</table>