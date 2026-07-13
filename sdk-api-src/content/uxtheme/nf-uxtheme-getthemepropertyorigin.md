---
UID: NF:uxtheme.GetThemePropertyOrigin
title: GetThemePropertyOrigin function (uxtheme.h)
description: Retrieves the location of the theme property definition for a property.
helpviewer_keywords: ["GetThemePropertyOrigin","GetThemePropertyOrigin function [Windows Controls]","controls.GetThemePropertyOrigin","controls.inet_GetThemePropertyOrigin","inet_GetThemePropertyOrigin","inet_GetThemePropertyOrigin_cpp","uxtheme/GetThemePropertyOrigin"]
old-location: controls\GetThemePropertyOrigin.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemepropertyorigin.htm
ms.date: 12/05/2018
ms.keywords: GetThemePropertyOrigin, GetThemePropertyOrigin function [Windows Controls], controls.GetThemePropertyOrigin, controls.inet_GetThemePropertyOrigin, inet_GetThemePropertyOrigin, inet_GetThemePropertyOrigin_cpp, uxtheme/GetThemePropertyOrigin
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
 - GetThemePropertyOrigin
 - uxtheme/GetThemePropertyOrigin
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
 - GetThemePropertyOrigin
---

# GetThemePropertyOrigin function


## -description

Retrieves the location of the theme property definition for a property.

## -parameters

### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata">OpenThemeData</a> to create an HTHEME.

### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part that contains the theme. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param iPropId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the property to retrieve. You may use any of the property values from Vssym32.h. These values are described in the reference pages for the functions that use them. For instance, the <a href="/windows/desktop/api/uxtheme/nf-uxtheme-getthemeint">GetThemeInt</a> function uses the TMT_BORDERSIZE value. See the <a href="/windows/desktop/Controls/uxctl-ref">Visual Styles Reference</a> for a list of functions.

### -param pOrigin [out]

Type: <b><a href="/windows/desktop/api/uxtheme/ne-uxtheme-propertyorigin">PROPERTYORIGIN</a>*</b>

Pointer to a <a href="/windows/desktop/api/uxtheme/ne-uxtheme-propertyorigin">PROPERTYORIGIN</a> enumerated type that indicates where the property was or was not found.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/Controls/property-typedefs">Property Identifiers</a>