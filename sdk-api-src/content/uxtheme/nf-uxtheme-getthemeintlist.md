---
UID: NF:uxtheme.GetThemeIntList
title: GetThemeIntList function (uxtheme.h)
description: Retrieves a list of int data from a visual style.
helpviewer_keywords: ["GetThemeIntList","GetThemeIntList function [Windows Controls]","controls.GetThemeIntList","controls.inet_GetThemeIntList","inet_GetThemeIntList","inet_GetThemeIntList_cpp","uxtheme/GetThemeIntList"]
old-location: controls\GetThemeIntList.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemeintlist.htm
ms.date: 12/05/2018
ms.keywords: GetThemeIntList, GetThemeIntList function [Windows Controls], controls.GetThemeIntList, controls.inet_GetThemeIntList, inet_GetThemeIntList, inet_GetThemeIntList_cpp, uxtheme/GetThemeIntList
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
 - GetThemeIntList
 - uxtheme/GetThemeIntList
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
 - GetThemeIntList
---

# GetThemeIntList function


## -description

Retrieves a list of <b>int</b> data from a visual style.

## -parameters

### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata">OpenThemeData</a> to create an HTHEME.

### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part that contains the list of data to return. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part. See <a href="/windows/desktop/Controls/parts-and-states">Parts and States</a>.

### -param iPropId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the property to retrieve. See <a href="/windows/desktop/Controls/property-typedefs">Property Identifiers</a>.

### -param pIntList [out]

Type: <b><a href="/windows/desktop/api/uxtheme/ns-uxtheme-intlist">INTLIST</a>*</b>

Pointer to an <a href="/windows/desktop/api/uxtheme/ns-uxtheme-intlist">INTLIST</a> structure that receives the <b>int</b> data.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful, otherwise an error code.

## -see-also

<a href="/windows/desktop/api/uxtheme/ns-uxtheme-intlist">INTLIST</a>