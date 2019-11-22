---
UID: NF:winerror.IS_ERROR
title: IS_ERROR macro (winerror.h)

description: Provides a generic test for errors on any status value.
old-location: com\is_error_macro.htm
tech.root: com
ms.assetid: 74497f4b-1c88-4c8a-b9e7-606e77364f48

ms.date: 12/05/2018
ms.keywords: IS_ERROR, IS_ERROR macro [COM], _com_IS_ERROR, com.is_error, com.is_error_macro, winerror/IS_ERROR
ms.topic: macro
f1_keywords: 
 - "winerror/IS_ERROR"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winerror.h
api_name:
 - IS_ERROR
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IS_ERROR macro


## -description


Provides a generic test for errors on any status value.




## -parameters




### -param Status

The status code. This value can be an <b>HRESULT</b> or an <b>SCODE</b>.


## -remarks



This macro is defined as follows:

<pre class="syntax" xml:space="preserve"><code>#define SEVERITY_ERROR     1
#define IS_ERROR(Status) (((unsigned long)(Status)) &gt;&gt; 31 == SEVERITY_ERROR)</code></pre>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/com/error-handling-in-com">Error Handling</a>
 

 

