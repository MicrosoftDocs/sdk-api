---
UID: NS:shtypes._STRRET
title: STRRET (shtypes.h)
description: Contains strings returned from the IShellFolder interface methods.
helpviewer_keywords: ["*LPSTRRET","LPSTRRET","LPSTRRET structure pointer [Windows Shell]","STRRET","STRRET structure [Windows Shell]","STRRET_CSTR","STRRET_OFFSET","STRRET_WSTR","_win32_STRRET","shell.STRRET","shtypes/LPSTRRET","shtypes/STRRET"]
old-location: shell\STRRET.htm
tech.root: shell
ms.assetid: 7868ef9b-07db-455b-b0be-ef0db7891447
ms.date: 12/05/2018
ms.keywords: '*LPSTRRET, LPSTRRET, LPSTRRET structure pointer [Windows Shell], STRRET, STRRET structure [Windows Shell], STRRET_CSTR, STRRET_OFFSET, STRRET_WSTR, _win32_STRRET, shell.STRRET, shtypes/LPSTRRET, shtypes/STRRET'
req.header: shtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: STRRET
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _STRRET
 - shtypes/_STRRET
 - STRRET
 - shtypes/STRRET
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shtypes.h
api_name:
 - STRRET
---

# STRRET structure


## -description

Contains strings returned from the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> interface methods.

## -struct-fields

### -field uType

Type: <b>UINT</b>

A value that specifies the desired format of the string. This can be one of the following values.



#### STRRET_CSTR

The string is returned in the <b>cStr</b> member.



#### STRRET_OFFSET

The <b>uOffset</b> member value indicates the number of bytes from the beginning of the item identifier list where the string is located.



#### STRRET_WSTR

The string is at the address specified by <b>pOleStr</b> member.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.pOleStr

Type: <b>LPWSTR</b>

A pointer to the string. This memory must be allocated with <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>. It is the calling application's responsibility to free this memory with <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> when it is no longer needed.

### -field DUMMYUNIONNAME.uOffset

Type: <b>UINT</b>

The offset into the item identifier list.

### -field DUMMYUNIONNAME.cStr

Type: <b>CHAR[MAX_PATH]</b>

The buffer to receive the display name.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof">IShellFolder::GetDisplayNameOf</a>