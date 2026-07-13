---
UID: NF:winnls.FILEMUIINFO_GET_MAIN_TYPEIDS
title: FILEMUIINFO_GET_MAIN_TYPEIDS macro (winnls.h)
description: Gets the main module types array associated with the type identifier offset information in the dwTypeIDMainOffset member of a FILEMUIINFO structure.
helpviewer_keywords: ["FILEMUIINFO_GET_MAIN_TYPEIDS","FILEMUIINFO_GET_MAIN_TYPEIDS macro [Internationalization for Windows Applications]","_win32_FILEMUIINFO_GET_MAIN_TYPEIDS","intl.filemuiinfo_get_main_typeids","winnls/FILEMUIINFO_GET_MAIN_TYPEIDS"]
old-location: intl\filemuiinfo_get_main_typeids.htm
tech.root: Intl
ms.assetid: ccdbf7c8-23a0-4b52-bf8c-8ae9f1a74281
ms.date: 07/01/2025
ms.keywords: FILEMUIINFO_GET_MAIN_TYPEIDS, FILEMUIINFO_GET_MAIN_TYPEIDS macro [Internationalization for Windows Applications], _win32_FILEMUIINFO_GET_MAIN_TYPEIDS, intl.filemuiinfo_get_main_typeids, winnls/FILEMUIINFO_GET_MAIN_TYPEIDS
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
 - FILEMUIINFO_GET_MAIN_TYPEIDS
 - winnls/FILEMUIINFO_GET_MAIN_TYPEIDS
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
 - FILEMUIINFO_GET_MAIN_TYPEIDS
---

# FILEMUIINFO_GET_MAIN_TYPEIDS macro

## -syntax

```cpp
DWORD* FILEMUIINFO_GET_MAIN_TYPEIDS(
    PFILEMUIINFO pInfo
);
```

## -returns

Type: **DWORD***

Returns a pointer to the main module types array. The macro returns **NULL** if the array is not initialized.


## -description

Gets the main module types array associated with the type identifier offset information in the <b>dwTypeIDMainOffset</b> member of a <a href="/windows/desktop/api/winnls/ns-winnls-filemuiinfo">FILEMUIINFO</a> structure.

## -parameters

### -param pInfo

Pointer to the <a href="/windows/desktop/api/winnls/ns-winnls-filemuiinfo">FILEMUIINFO</a> structure.

## -see-also

<a href="/windows/desktop/api/winnls/ns-winnls-filemuiinfo">FILEMUIINFO</a>



<a href="/windows/desktop/Intl/multilingual-user-interface">Multilingual User Interface</a>



<a href="/windows/desktop/Intl/multilingual-user-interface-macros">Multilingual User Interface Macros</a>
