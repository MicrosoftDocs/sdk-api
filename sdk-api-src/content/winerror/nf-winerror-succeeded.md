---
UID: NF:winerror.SUCCEEDED
title: SUCCEEDED macro (winerror.h)
description: Provides a generic test for success on any status value.
helpviewer_keywords: ["SUCCEEDED","SUCCEEDED macro [COM]","_com_SUCCEEDED","com.succeeded","com.succeeded_macro","winerror/SUCCEEDED"]
old-location: com\succeeded_macro.htm
tech.root: com
ms.assetid: 7a258b0b-d214-46c5-be0a-6493cd14a0e5
ms.date: 12/05/2018
ms.keywords: SUCCEEDED, SUCCEEDED macro [COM], _com_SUCCEEDED, com.succeeded, com.succeeded_macro, winerror/SUCCEEDED
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
 - SUCCEEDED
 - winerror/SUCCEEDED
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
 - SUCCEEDED
---

# SUCCEEDED macro


## -description

Provides a generic test for success on any status value.

## -parameters

### -param hr

The status code. This value can be an <b>HRESULT</b> or an <b>SCODE</b>. A non-negative number indicates success.

## -remarks

This macro is defined as follows:


``` syntax
#define SUCCEEDED(hr) (((HRESULT)(hr)) >= 0)
```


## -see-also

<a href="/windows/desktop/com/error-handling-in-com">Error Handling</a>
