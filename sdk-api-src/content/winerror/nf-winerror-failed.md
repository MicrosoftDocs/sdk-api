---
UID: NF:winerror.FAILED
title: FAILED macro (winerror.h)
description: Provides a generic test for failure on any status value.
helpviewer_keywords: ["FAILED","FAILED macro [COM]","_com_FAILED","com.failed","com.failed_macro","winerror/FAILED"]
old-location: com\failed_macro.htm
tech.root: com
ms.assetid: d9c4ff73-c255-4a82-b901-23bd5b41ee6c
ms.date: 12/05/2018
ms.keywords: FAILED, FAILED macro [COM], _com_FAILED, com.failed, com.failed_macro, winerror/FAILED
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
 - FAILED
 - winerror/FAILED
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
 - FAILED
---

# FAILED macro


## -description

Provides a generic test for failure on any status value.

## -parameters

### -param hr

The status code. This value can be an <b>HRESULT</b> or an <b>SCODE</b>. A negative number indicates failure.

## -remarks

This macro is defined as follows:


``` syntax
#define FAILED(hr) (((HRESULT)(hr)) < 0)
```


## -see-also

<a href="/windows/desktop/com/error-handling-in-com">Error Handling</a>
