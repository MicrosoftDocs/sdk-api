---
UID: NF:winerror.SCODE_CODE
title: SCODE_CODE macro
author: windows-sdk-content
description: Extracts the code portion of the specified SCODE.
old-location: com\scode_code_macro.htm
old-project: com
ms.assetid: 878456dc-3da4-470a-b9cc-16018f540c17
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: SCODE_CODE, SCODE_CODE macro [COM], _com_SCODE_CODE, com.scode_code, com.scode_code_macro, winerror/SCODE_CODE
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: ENCRYPTION_CERTIFICATE_LIST, *PENCRYPTION_CERTIFICATE_LIST
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winerror.h
api_name:
 - SCODE_CODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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




<a href="https://msdn.microsoft.com/library/windows/hardware/ff544310">Error Handling</a>
 

 

