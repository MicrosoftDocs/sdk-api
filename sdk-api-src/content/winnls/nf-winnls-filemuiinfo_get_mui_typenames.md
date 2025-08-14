---
UID: NF:winnls.FILEMUIINFO_GET_MUI_TYPENAMES
title: FILEMUIINFO_GET_MUI_TYPENAMES macro (winnls.h)
description: Gets the MUI module names multistring array associated with the type name offset information in the dwTypeNameMUIOffset member of a FILEMUIINFO structure.
helpviewer_keywords: ["FILEMUIINFO_GET_MUI_TYPENAMES","FILEMUIINFO_GET_MUI_TYPENAMES macro [Internationalization for Windows Applications]","_win32_FILEMUIINFO_GET_MUI_TYPENAMES","intl.filemuiinfo_get_mui_typenames","winnls/FILEMUIINFO_GET_MUI_TYPENAMES"]
old-location: intl\filemuiinfo_get_mui_typenames.htm
tech.root: Intl
ms.assetid: e2fae2ab-dfde-4efd-af83-9818322619ad
ms.date: 07/01/2025
ms.keywords: FILEMUIINFO_GET_MUI_TYPENAMES, FILEMUIINFO_GET_MUI_TYPENAMES macro [Internationalization for Windows Applications], _win32_FILEMUIINFO_GET_MUI_TYPENAMES, intl.filemuiinfo_get_mui_typenames, winnls/FILEMUIINFO_GET_MUI_TYPENAMES
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FILEMUIINFO_GET_MUI_TYPENAMES
 - winnls/FILEMUIINFO_GET_MUI_TYPENAMES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnls.h
api_name:
 - FILEMUIINFO_GET_MUI_TYPENAMES
---

# FILEMUIINFO_GET_MUI_TYPENAMES macro

## -syntax

```cpp
LPWSTR FILEMUIINFO_GET_MUI_TYPENAMES(
    PFILEMUIINFO pInfo
);
```

## -returns

Type: **LPWSTR**

Returns a pointer to the MUI module names multistring array. The macro returns **NULL** if the array is not initialized.


## -description

Gets the MUI module names multistring array associated with the type name offset information in the <b>dwTypeNameMUIOffset</b> member of a <a href="/windows/desktop/api/winnls/ns-winnls-filemuiinfo">FILEMUIINFO</a> structure.

## -parameters

### -param pInfo

Pointer to the <a href="/windows/desktop/api/winnls/ns-winnls-filemuiinfo">FILEMUIINFO</a> structure.

## -see-also

<a href="/windows/desktop/api/winnls/ns-winnls-filemuiinfo">FILEMUIINFO</a>



<a href="/windows/desktop/Intl/multilingual-user-interface">Multilingual User Interface</a>



<a href="/windows/desktop/Intl/multilingual-user-interface-macros">Multilingual User Interface Macros</a>
