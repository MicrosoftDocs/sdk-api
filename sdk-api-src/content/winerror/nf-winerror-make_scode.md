---
UID: NF:winerror.MAKE_SCODE
title: MAKE_SCODE macro (winerror.h)
description: Creates an SCODE value from its component pieces.
helpviewer_keywords: ["MAKE_SCODE","MAKE_SCODE macro [COM]","_com_MAKE_SCODE","com.make_scode","com.make_scode_macro","winerror/MAKE_SCODE"]
old-location: com\make_scode_macro.htm
tech.root: com
ms.assetid: b7d32bf7-39b3-4fb1-8fe1-b3aedc74b582
ms.date: 12/05/2018
ms.keywords: MAKE_SCODE, MAKE_SCODE macro [COM], _com_MAKE_SCODE, com.make_scode, com.make_scode_macro, winerror/MAKE_SCODE
f1_keywords:
- winerror/MAKE_SCODE
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
- MAKE_SCODE
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/com/error-handling-in-com">Error Handling</a>
 

 

