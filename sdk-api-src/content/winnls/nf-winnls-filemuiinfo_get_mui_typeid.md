---
UID: NF:winnls.FILEMUIINFO_GET_MUI_TYPEID
title: FILEMUIINFO_GET_MUI_TYPEID macro (winnls.h)
description: Gets the MUI module types array element associated with the type identifier size and offset information in a FILEMUIINFO structure. The information is provided in the dwTypeIDMUISize and dwTypeIDMUIOffset members of the structure.
helpviewer_keywords: ["FILEMUIINFO_GET_MUI_TYPEID","FILEMUIINFO_GET_MUI_TYPEID macro [Internationalization for Windows Applications]","_win32_FILEMUIINFO_GET_MUI_TYPEID","intl.filemuiinfo_get_mui_typeid","winnls/FILEMUIINFO_GET_MUI_TYPEID"]
old-location: intl\filemuiinfo_get_mui_typeid.htm
tech.root: Intl
ms.assetid: 212bd5ea-468f-4096-8199-d84c32f30d53
ms.date: 07/01/2025
ms.keywords: FILEMUIINFO_GET_MUI_TYPEID, FILEMUIINFO_GET_MUI_TYPEID macro [Internationalization for Windows Applications], _win32_FILEMUIINFO_GET_MUI_TYPEID, intl.filemuiinfo_get_mui_typeid, winnls/FILEMUIINFO_GET_MUI_TYPEID
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
 - FILEMUIINFO_GET_MUI_TYPEID
 - winnls/FILEMUIINFO_GET_MUI_TYPEID
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
 - FILEMUIINFO_GET_MUI_TYPEID
---

# FILEMUIINFO_GET_MUI_TYPEID macro

## -syntax

```cpp
DWORD FILEMUIINFO_GET_MUI_TYPEID(
    PFILEMUIINFO pInfo,
    DWORD iType
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns the MUI module types array element. The macro returns **NULL** if the array is not initialized or if the supplied index is out of bounds.


## -description

Gets the MUI module types array element associated with the type identifier size and offset information in a <a href="/windows/desktop/api/winnls/ns-winnls-filemuiinfo">FILEMUIINFO</a> structure. The information is provided in the <b>dwTypeIDMUISize</b> and <b>dwTypeIDMUIOffset</b> members of the structure.

## -parameters

### -param pInfo

Pointer to the <a href="/windows/desktop/api/winnls/ns-winnls-filemuiinfo">FILEMUIINFO</a> structure.

### -param iType

Index of the array element.

## -see-also

<a href="/windows/desktop/api/winnls/ns-winnls-filemuiinfo">FILEMUIINFO</a>



<a href="/windows/desktop/Intl/multilingual-user-interface">Multilingual User Interface</a>



<a href="/windows/desktop/Intl/multilingual-user-interface-macros">Multilingual User Interface Macros</a>
