---
UID: NF:uxtheme.GetThemeTextMetrics
title: GetThemeTextMetrics function (uxtheme.h)
description: Retrieves information about the font specified by a visual style for a particular part.
helpviewer_keywords: ["GetThemeTextMetrics","GetThemeTextMetrics function [Windows Controls]","controls.GetThemeTextMetrics","controls.inet_GetThemeTextMetrics","inet_GetThemeTextMetrics","inet_GetThemeTextMetrics_cpp","uxtheme/GetThemeTextMetrics"]
old-location: controls\GetThemeTextMetrics.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemetextmetrics.htm
ms.date: 12/05/2018
ms.keywords: GetThemeTextMetrics, GetThemeTextMetrics function [Windows Controls], controls.GetThemeTextMetrics, controls.inet_GetThemeTextMetrics, inet_GetThemeTextMetrics, inet_GetThemeTextMetrics_cpp, uxtheme/GetThemeTextMetrics
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
 - GetThemeTextMetrics
 - uxtheme/GetThemeTextMetrics
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
 - GetThemeTextMetrics
---

# GetThemeTextMetrics function


## -description

Retrieves information about the font specified by a visual style for a particular part.

## -parameters

### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata">OpenThemeData</a> to create an HTHEME.

### -param hdc [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HDC</a></b>

HDC to use for screen context. This parameter may be set to <b>NULL</b>.

### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part to retrieve font information about. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param ptm [out]

Type: <b><a href="/windows/desktop/api/wingdi/ns-wingdi-textmetrica">TEXTMETRIC</a>*</b>

Receives the font information.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/Controls/property-typedefs">Property Identifiers</a>