---
UID: NF:winerror.SCODE_CODE
title: SCODE_CODE macro (winerror.h)
description: Extracts the code portion of the specified SCODE.
helpviewer_keywords: ["SCODE_CODE","SCODE_CODE macro [COM]","_com_SCODE_CODE","com.scode_code","com.scode_code_macro","winerror/SCODE_CODE"]
old-location: com\scode_code_macro.htm
tech.root: com
ms.assetid: 878456dc-3da4-470a-b9cc-16018f540c17
ms.date: 12/05/2018
ms.keywords: SCODE_CODE, SCODE_CODE macro [COM], _com_SCODE_CODE, com.scode_code, com.scode_code_macro, winerror/SCODE_CODE
f1_keywords:
- winerror/SCODE_CODE
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
- SCODE_CODE
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SCODE_CODE macro


## -description


Extracts the code portion of the specified <b>SCODE</b>. 


## -parameters




### -param sc

The status code.


## -remarks



This macro is defined as follows:

<pre class="syntax" xml:space="preserve"><code>#define SCODE_CODE(sc)      ((sc) &amp; 0xFFFF)</code></pre>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/com/error-handling-in-com">Error Handling</a>
 

 

