---
UID: NF:uxtheme.GetThemeString
title: GetThemeString function (uxtheme.h)
description: Retrieves the value of a string property.
helpviewer_keywords: ["GetThemeString","GetThemeString function [Windows Controls]","controls.GetThemeString","controls.inet_GetThemeString","inet_GetThemeString","inet_GetThemeString_cpp","uxtheme/GetThemeString"]
old-location: controls\GetThemeString.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemestring.htm
ms.date: 12/05/2018
ms.keywords: GetThemeString, GetThemeString function [Windows Controls], controls.GetThemeString, controls.inet_GetThemeString, inet_GetThemeString, inet_GetThemeString_cpp, uxtheme/GetThemeString
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
 - GetThemeString
 - uxtheme/GetThemeString
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
 - GetThemeString
---

# GetThemeString function


## -description

Retrieves the value of a string property.

## -parameters

### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata">OpenThemeData</a> to create an HTHEME.

### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part containing the string property. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param iPropId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the property to retrieve. For a list of possible values, see <a href="/windows/desktop/Controls/property-typedefs">Property Identifiers</a>.

### -param pszBuff [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPWSTR</a></b>

Pointer to a buffer that receives the string value.

### -param cchMaxBuffChars [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the maximum number of characters <i>pszBuff</i> can contain.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/Controls/property-typedefs">Property Identifiers</a>