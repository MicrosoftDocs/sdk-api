---
UID: NF:winerror.SCODE_FACILITY
title: SCODE_FACILITY macro (winerror.h)
description: Extracts the facility of the specified SCODE.
helpviewer_keywords: ["SCODE_FACILITY","SCODE_FACILITY macro [COM]","_com_SCODE_FACILITY","com.scode_facility","com.scode_facility_macro","winerror/SCODE_FACILITY"]
old-location: com\scode_facility_macro.htm
tech.root: com
ms.assetid: 646e2d98-69c4-43ac-b939-c67a61d7cbce
ms.date: 12/05/2018
ms.keywords: SCODE_FACILITY, SCODE_FACILITY macro [COM], _com_SCODE_FACILITY, com.scode_facility, com.scode_facility_macro, winerror/SCODE_FACILITY
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
 - SCODE_FACILITY
 - winerror/SCODE_FACILITY
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
 - SCODE_FACILITY
---

# SCODE_FACILITY macro


## -description

Extracts the facility of the specified <b>SCODE</b>.

## -parameters

### -param sc

The status code.

## -remarks

This macro is defined as follows:


``` syntax
#define SCODE_FACILITY(sc)    (((sc) >> 16) & 0x1fff)
```


## -see-also

<a href="/windows/desktop/com/error-handling-in-com">Error Handling</a>
