---
UID: NF:uxtheme.GetThemeFont
title: GetThemeFont function (uxtheme.h)
description: Retrieves the value of a font property.
helpviewer_keywords: ["GetThemeFont","GetThemeFont function [Windows Controls]","controls.GetThemeFont","controls.inet_GetThemeFont","inet_GetThemeFont","inet_GetThemeFont_cpp","uxtheme/GetThemeFont"]
old-location: controls\GetThemeFont.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemefont.htm
ms.date: 12/05/2018
ms.keywords: GetThemeFont, GetThemeFont function [Windows Controls], controls.GetThemeFont, controls.inet_GetThemeFont, inet_GetThemeFont, inet_GetThemeFont_cpp, uxtheme/GetThemeFont
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
 - GetThemeFont
 - uxtheme/GetThemeFont
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
 - GetThemeFont
---

# GetThemeFont function


## -description

Retrieves the value of a font property.

## -parameters

### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata">OpenThemeData</a> to create an HTHEME.

### -param hdc [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HDC</a></b>

HDC. This parameter may be set to <b>NULL</b>.

### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part that contains the font property. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param iPropId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the property to retrieve. For a list of possible values, see <a href="/windows/desktop/Controls/property-typedefs">Property Identifiers</a>.

### -param pFont [out]

Type: <b>LOGFONTW*</b>

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure that receives the font property value.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The font is scaled in dots per inch (DPI)  for the current logical screen.

If the property is not supported for the specified part and state, E_PROP_ID_UNSUPPORTED may be returned.

## -see-also

<a href="/windows/desktop/Controls/property-typedefs">Property Identifiers</a>