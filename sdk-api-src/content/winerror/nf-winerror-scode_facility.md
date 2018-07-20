---
UID: NF:winerror.SCODE_FACILITY
title: SCODE_FACILITY macro
author: windows-sdk-content
description: Extracts the facility of the specified SCODE.
old-location: com\scode_facility_macro.htm
old-project: com
ms.assetid: 646e2d98-69c4-43ac-b939-c67a61d7cbce
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: SCODE_FACILITY, SCODE_FACILITY macro [COM], _com_SCODE_FACILITY, com.scode_facility, com.scode_facility_macro, winerror/SCODE_FACILITY
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
 - SCODE_FACILITY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# SCODE_FACILITY macro


## -description


Extracts the facility of the specified <b>SCODE</b>. 


## -parameters




### -param sc

The status code.


## -remarks



This macro is defined as follows:

<pre class="syntax" xml:space="preserve"><code>#define SCODE_FACILITY(sc)    (((sc) &gt;&gt; 16) &amp; 0x1fff)</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff544310">Error Handling</a>
 

 

