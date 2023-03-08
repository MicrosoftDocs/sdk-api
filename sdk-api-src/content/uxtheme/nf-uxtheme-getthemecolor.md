---
UID: NF:uxtheme.GetThemeColor
title: GetThemeColor function (uxtheme.h)
description: Retrieves the value of a color property.
helpviewer_keywords: ["GetThemeColor","GetThemeColor function [Windows Controls]","controls.GetThemeColor","controls.inet_GetThemeColor","inet_GetThemeColor","inet_GetThemeColor_cpp","uxtheme/GetThemeColor"]
old-location: controls\GetThemeColor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemecolor.htm
ms.date: 12/05/2018
ms.keywords: GetThemeColor, GetThemeColor function [Windows Controls], controls.GetThemeColor, controls.inet_GetThemeColor, inet_GetThemeColor, inet_GetThemeColor_cpp, uxtheme/GetThemeColor
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
 - GetThemeColor
 - uxtheme/GetThemeColor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - UxTheme.dll
 - Ext-MS-Win-UXTheme-Themes-l1-1-0.dll
 - xamlpalwp.dll
 - ext-ms-win-uxtheme-themes-l1-1-1.dll
api_name:
 - GetThemeColor
---

# GetThemeColor function


## -description

Retrieves the value of a color property.

## -parameters

### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata">OpenThemeData</a> to create an HTHEME.

### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part that contains the color property. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param iPropId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the property to retrieve. For a list of possible values, see <a href="/windows/desktop/Controls/property-typedefs">Property Identifiers</a>.

### -param pColor [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a>*</b>

Pointer to a <a href="/windows/desktop/gdi/colorref">COLORREF</a> structure that receives the color value.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/Controls/property-typedefs">Property Identifiers</a>