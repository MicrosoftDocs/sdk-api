---
UID: NF:winerror.SCODE_SEVERITY
title: SCODE_SEVERITY macro (winerror.h)
description: Extracts the severity field of the specified SCODE.
helpviewer_keywords: ["SCODE_SEVERITY","SCODE_SEVERITY macro [COM]","_com_SCODE_SEVERITY","com.scode_severity","com.scode_severity_macro","winerror/SCODE_SEVERITY"]
old-location: com\scode_severity_macro.htm
tech.root: com
ms.assetid: a1193f0c-e53e-4e63-b801-f1237bee29a1
ms.date: 12/05/2018
ms.keywords: SCODE_SEVERITY, SCODE_SEVERITY macro [COM], _com_SCODE_SEVERITY, com.scode_severity, com.scode_severity_macro, winerror/SCODE_SEVERITY
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
 - SCODE_SEVERITY
 - winerror/SCODE_SEVERITY
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
 - SCODE_SEVERITY
---

# SCODE_SEVERITY macro


## -description

Extracts the severity field of the specified <b>SCODE</b>.

## -parameters

### -param sc

The status code.

## -remarks

This macro is defined as follows:


``` syntax
#define SCODE_SEVERITY(sc)    (((sc) >> 31) & 0x1)
```


## -see-also

<a href="/windows/desktop/com/error-handling-in-com">Error Handling</a>
