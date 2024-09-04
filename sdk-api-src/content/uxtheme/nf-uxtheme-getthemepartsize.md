---
UID: NF:uxtheme.GetThemePartSize
title: GetThemePartSize function (uxtheme.h)
description: Calculates the original size of the part defined by a visual style.
helpviewer_keywords: ["GetThemePartSize","GetThemePartSize function [Windows Controls]","controls.GetThemePartSize","controls.inet_GetThemePartSize","inet_GetThemePartSize","inet_GetThemePartSize_cpp","uxtheme/GetThemePartSize"]
old-location: controls\GetThemePartSize.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemepartsize.htm
ms.date: 12/05/2018
ms.keywords: GetThemePartSize, GetThemePartSize function [Windows Controls], controls.GetThemePartSize, controls.inet_GetThemePartSize, inet_GetThemePartSize, inet_GetThemePartSize_cpp, uxtheme/GetThemePartSize
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
 - GetThemePartSize
 - uxtheme/GetThemePartSize
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
 - GetThemePartSize
---

# GetThemePartSize function


## -description

Calculates the original size of the part defined by a visual style.

## -parameters

### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata">OpenThemeData</a> to create an HTHEME.

### -param hdc [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HDC</a></b>

HDC to select fonts into.

### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part to calculate the size of. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param prc [in]

Type: <b>LPCRECT</b>

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the rectangle used for the part drawing destination. This parameter may be set to <b>NULL</b>.

### -param eSize [in]

Type: <b>THEMESIZE</b>

Enumerated type that specifies the type of size to retrieve. See <a href="/windows/desktop/api/uxtheme/ne-uxtheme-themesize">THEMESIZE</a> for a list of type values.

### -param psz [out]

Type: <b><a href="/windows/win32/api/windef/ns-windef-size">SIZE</a>*</b>

Pointer to a <a href="/windows/win32/api/windef/ns-windef-size">SIZE</a> structure that receives the dimensions of the specified part.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/Controls/property-typedefs">Property Identifiers</a>