---
UID: NF:winerror.HRESULT_FROM_WIN32
title: HRESULT_FROM_WIN32 macro (winerror.h)
description: Maps a system error code to an HRESULT value.
helpviewer_keywords: ["HRESULT_FROM_WIN32","HRESULT_FROM_WIN32 macro [COM]","_com_HRESULT_FROM_WIN32","com.hresult_from_win32","com.hresult_from_win32_macro","winerror/HRESULT_FROM_WIN32"]
old-location: com\hresult_from_win32_macro.htm
tech.root: com
ms.assetid: 40e6f80d-a778-4d5f-bb1b-db294815f8b5
ms.date: 12/05/2018
ms.keywords: HRESULT_FROM_WIN32, HRESULT_FROM_WIN32 macro [COM], _com_HRESULT_FROM_WIN32, com.hresult_from_win32, com.hresult_from_win32_macro, winerror/HRESULT_FROM_WIN32
req.header: winerror.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HRESULT_FROM_WIN32
 - winerror/HRESULT_FROM_WIN32
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winerror.h
api_name:
 - HRESULT_FROM_WIN32
---

# HRESULT_FROM_WIN32 macro


## -description

Maps a <a href="/windows/desktop/Debug/system-error-codes">system error code</a> to an <b>HRESULT</b> value.

## -parameters

### -param x

The system error code.

## -remarks

This macro is defined as follows:


``` syntax
//
// HRESULT_FROM_WIN32(x) used to be a macro, however we now run it as an inline function
// to prevent double evaluation of 'x'. If you still need the macro, you can use __HRESULT_FROM_WIN32(x)
//
#define __HRESULT_FROM_WIN32(x) ((HRESULT)(x) <= 0 ? ((HRESULT)(x)) : ((HRESULT) (((x) & 0x0000FFFF) | (FACILITY_WIN32 << 16) | 0x80000000)))

#ifndef __midl
FORCEINLINE HRESULT HRESULT_FROM_WIN32(unsigned long x) { 
   return (HRESULT)(x) <= 0 ? (HRESULT)(x) : (HRESULT) (((x) & 0x0000FFFF) | (FACILITY_WIN32 << 16) | 0x80000000);
}
#else
#define HRESULT_FROM_WIN32(x) __HRESULT_FROM_WIN32(x)
#endif


```


## -see-also

<a href="/windows/desktop/com/error-handling-in-com">Error Handling</a>
