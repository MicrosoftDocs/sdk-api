---
UID: NF:winerror.HRESULT_CODE
title: HRESULT_CODE macro
author: windows-driver-content
description: Extracts the code portion of the specified HRESULT.
old-location: com\hresult_code_macro.htm
old-project: com
ms.assetid: 20f3b51d-38b6-4989-b9c2-5b08012a7352
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: HRESULT_CODE, HRESULT_CODE macro [COM], _com_HRESULT_CODE, com.hresult_code, com.hresult_code_macro, winerror/HRESULT_CODE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
req.typenames: ENCRYPTION_CERTIFICATE_LIST, *PENCRYPTION_CERTIFICATE_LIST
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winerror.h
api_name:
-	HRESULT_CODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# HRESULT_CODE macro


## -description


Extracts the code portion of the specified <b>HRESULT</b>.


## -parameters




### -param hr

The <b>HRESULT</b> value.


## -remarks



This macro is defined as follows:

<pre class="syntax" xml:space="preserve"><code>#define HRESULT_CODE(hr)    ((hr) &amp; 0xFFFF)</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff544310">Error Handling</a>
 

 

