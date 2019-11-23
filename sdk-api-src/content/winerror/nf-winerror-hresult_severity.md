---
UID: NF:winerror.HRESULT_SEVERITY
title: HRESULT_SEVERITY macro (winerror.h)

description: Extracts the severity field of the specified HRESULT.
old-location: com\hresult_severity_macro.htm
tech.root: com
ms.assetid: e574ddc2-e950-4618-bc16-1b99989a4a68

ms.date: 12/05/2018
ms.keywords: HRESULT_SEVERITY, HRESULT_SEVERITY macro [COM], _com_HRESULT_SEVERITY, com.hresult_severity, com.hresult_severity_macro, winerror/HRESULT_SEVERITY
ms.topic: macro
f1_keywords: 
 - "winerror/HRESULT_SEVERITY"
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
 - HRESULT_SEVERITY
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# HRESULT_SEVERITY macro


## -description


Extracts the severity field of the specified <b>HRESULT</b>.


## -parameters




### -param hr

The <b>HRESULT</b>.


## -remarks



This macro is defined as follows:

<pre class="syntax" xml:space="preserve"><code>#define HRESULT_SEVERITY(hr)  (((hr) &gt;&gt; 31) &amp; 0x1)</code></pre>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/com/error-handling-in-com">Error Handling</a>
 

 

