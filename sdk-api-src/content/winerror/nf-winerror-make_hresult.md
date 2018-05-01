---
UID: NF:winerror.MAKE_HRESULT
title: MAKE_HRESULT macro
author: windows-driver-content
description: Creates an HRESULT value from its component pieces.
old-location: com\make_hresult_macro.htm
old-project: com
ms.assetid: f9624cbd-35a4-4e44-a796-cf463366299a
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: MAKE_HRESULT, MAKE_HRESULT macro [COM], _com_MAKE_HRESULT, com.make_hresult, com.make_hresult_macro, dmerror/MAKE_HRESULT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: winerror.h
req.include-header: Winerror.h, Ddrawi.h, Ddrawint.h, Winerror.h, Ddrawi.h, Ddrawint.h
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
-	dmerror.h
api_name:
-	MAKE_HRESULT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# MAKE_HRESULT macro


## -description


Creates an <b>HRESULT</b> value from its component pieces.


## -parameters




### -param sev

The severity.


### -param fac

The facility.


### -param code

The code.


## -remarks



This macro is defined as follows:

<pre class="syntax" xml:space="preserve"><code>#define MAKE_HRESULT(sev,fac,code) \
    ((HRESULT) (((unsigned long)(sev)&lt;&lt;31) | ((unsigned long)(fac)&lt;&lt;16) | ((unsigned long)(code))) )</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff544310">Error Handling</a>
 

 

