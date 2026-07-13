---
UID: NF:winnls.FILEMUIINFO_GET_MAIN_TYPENAMES
title: FILEMUIINFO_GET_MAIN_TYPENAMES macro (winnls.h)
description: Gets the main module names multistring array associated with the type name offset information in the dwTypeNameMainOffset member of a FILEMUIINFO structure.
helpviewer_keywords: ["FILEMUIINFO_GET_MAIN_TYPENAMES","FILEMUIINFO_GET_MAIN_TYPENAMES macro [Internationalization for Windows Applications]","_win32_FILEMUIINFO_GET_MAIN_TYPENAMES","intl.filemuiinfo_get_main_typenames","winnls/FILEMUIINFO_GET_MAIN_TYPENAMES"]
old-location: intl\filemuiinfo_get_main_typenames.htm
tech.root: Intl
ms.assetid: 93fe7be8-693f-493c-94d4-7b7b2405880a
ms.date: 07/01/2025
ms.keywords: FILEMUIINFO_GET_MAIN_TYPENAMES, FILEMUIINFO_GET_MAIN_TYPENAMES macro [Internationalization for Windows Applications], _win32_FILEMUIINFO_GET_MAIN_TYPENAMES, intl.filemuiinfo_get_main_typenames, winnls/FILEMUIINFO_GET_MAIN_TYPENAMES
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
 - FILEMUIINFO_GET_MAIN_TYPENAMES
 - winnls/FILEMUIINFO_GET_MAIN_TYPENAMES
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
 - FILEMUIINFO_GET_MAIN_TYPENAMES
---

# FILEMUIINFO_GET_MAIN_TYPENAMES macro

## -syntax

```cpp
LPWSTR FILEMUIINFO_GET_MAIN_TYPENAMES(
    PFILEMUIINFO pInfo
);
```

## -returns

Type: **LPWSTR**

Returns a pointer to the main module names multistring array. The macro returns **NULL** if the array is not initialized.


## -description

Gets the main module names multistring array associated with the type name offset information in the <b>dwTypeNameMainOffset</b> member of a <a href="/windows/desktop/api/winnls/ns-winnls-filemuiinfo">FILEMUIINFO</a> structure.

## -parameters

### -param pInfo

Pointer to the <a href="/windows/desktop/api/winnls/ns-winnls-filemuiinfo">FILEMUIINFO</a> structure.

## -see-also

<a href="/windows/desktop/api/winnls/ns-winnls-filemuiinfo">FILEMUIINFO</a>



<a href="/windows/desktop/Intl/multilingual-user-interface">Multilingual User Interface</a>



<a href="/windows/desktop/Intl/multilingual-user-interface-macros">Multilingual User Interface Macros</a>
