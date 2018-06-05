---
UID: NF:winerror.MAKE_SCODE
title: MAKE_SCODE macro
author: windows-sdk-content
description: Creates an SCODE value from its component pieces.
old-location: com\make_scode_macro.htm
old-project: com
ms.assetid: b7d32bf7-39b3-4fb1-8fe1-b3aedc74b582
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: MAKE_SCODE, MAKE_SCODE macro [COM], _com_MAKE_SCODE, com.make_scode, com.make_scode_macro, winerror/MAKE_SCODE
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
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winerror.h
api_name:
-	MAKE_SCODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# MAKE_SCODE macro


## -description


Creates an <b>SCODE</b> value from its component pieces.


## -parameters




### -param sev

The severity.


### -param fac

The facility.


### -param code

The code.


## -remarks



This macro is defined as follows:

<pre class="syntax" xml:space="preserve"><code>#define MAKE_SCODE(sev,fac,code) \
    ((SCODE) (((unsigned long)(sev)&lt;&lt;31) | ((unsigned long)(fac)&lt;&lt;16) | ((unsigned long)(code))) )</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff544310">Error Handling</a>
 

 

