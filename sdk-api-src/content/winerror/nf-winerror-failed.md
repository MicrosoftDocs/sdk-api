---
UID: NF:winerror.FAILED
title: FAILED macro (winerror.h)
author: windows-sdk-content
description: Provides a generic test for failure on any status value.
old-location: com\failed_macro.htm
tech.root: com
ms.assetid: d9c4ff73-c255-4a82-b901-23bd5b41ee6c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FAILED, FAILED macro [COM], _com_FAILED, com.failed, com.failed_macro, winerror/FAILED
ms.topic: macro
f1_keywords: ["winerror/FAILED"]
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
 - FAILED
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FAILED macro


## -description


Provides a generic test for failure on any status value. 


## -parameters




### -param hr

The status code. This value can be an <b>HRESULT</b> or an <b>SCODE</b>. A negative number indicates failure.


## -remarks



This macro is defined as follows:

<pre class="syntax" xml:space="preserve"><code>#define FAILED(hr) (((HRESULT)(hr)) &lt; 0)</code></pre>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/com/error-handling-in-com">Error Handling</a>
 

 

