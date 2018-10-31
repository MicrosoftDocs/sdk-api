---
UID: NF:winerror.HRESULT_CODE
title: HRESULT_CODE macro
author: windows-sdk-content
description: Extracts the code portion of the specified HRESULT.
old-location: com\hresult_code_macro.htm
tech.root: com
ms.assetid: 20f3b51d-38b6-4989-b9c2-5b08012a7352
ms.author: windowssdkdev
ms.date: 10/30/2018
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
 - HRESULT_CODE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling</a>
 

 

