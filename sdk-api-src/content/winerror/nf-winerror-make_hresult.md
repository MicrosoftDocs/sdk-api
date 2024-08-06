---
UID: NF:winerror.MAKE_HRESULT
title: MAKE_HRESULT macro (winerror.h)
description: The MAKE_HRESULT macro (winerror.h) creates an HRESULT value from its component pieces.
helpviewer_keywords: ["MAKE_HRESULT","MAKE_HRESULT macro [COM]","_com_MAKE_HRESULT","com.make_hresult","com.make_hresult_macro","dmerror/MAKE_HRESULT"]
old-location: com\make_hresult_macro.htm
tech.root: com
ms.assetid: f9624cbd-35a4-4e44-a796-cf463366299a
ms.date: 08/15/2022
ms.keywords: MAKE_HRESULT, MAKE_HRESULT macro [COM], _com_MAKE_HRESULT, com.make_hresult, com.make_hresult_macro, dmerror/MAKE_HRESULT
req.header: winerror.h
req.include-header: Winerror.h, Ddrawi.h, Ddrawint.h, Winerror.h, Ddrawi.h, Ddrawint.h
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
 - MAKE_HRESULT
 - winerror/MAKE_HRESULT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dmerror.h
api_name:
 - MAKE_HRESULT
---

# MAKE_HRESULT macro


## -description

Creates an <b>HRESULT</b> value from its component pieces.

## -parameters

### -param sev

The severity.

### -param fac

The facility.

### -param code

The code.

## -remarks

This macro is defined as follows:


``` syntax
#define MAKE_HRESULT(sev,fac,code) \
    ((HRESULT) (((unsigned long)(sev)<<31) | ((unsigned long)(fac)<<16) | ((unsigned long)(code))) )
```


## -see-also

<a href="/windows/desktop/com/error-handling-in-com">Error Handling</a>
