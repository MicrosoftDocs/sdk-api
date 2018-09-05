---
UID: NF:winerror.SCODE_SEVERITY
title: SCODE_SEVERITY macro
author: windows-sdk-content
description: Extracts the severity field of the specified SCODE.
old-location: com\scode_severity_macro.htm
old-project: com
ms.assetid: a1193f0c-e53e-4e63-b801-f1237bee29a1
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: SCODE_SEVERITY, SCODE_SEVERITY macro [COM], _com_SCODE_SEVERITY, com.scode_severity, com.scode_severity_macro, winerror/SCODE_SEVERITY
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: winerror.h
req.include-header: 
req.redist: 
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
 - SCODE_SEVERITY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# SCODE_SEVERITY macro


## -description


Extracts the severity field of the specified <b>SCODE</b>. 


## -parameters




### -param sc

The status code.


## -remarks



This macro is defined as follows:

<pre class="syntax" xml:space="preserve"><code>#define SCODE_SEVERITY(sc)    (((sc) &gt;&gt; 31) &amp; 0x1)</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling</a>
 

 

