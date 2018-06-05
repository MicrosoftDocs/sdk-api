---
UID: NF:winerror.HRESULT_FACILITY
title: HRESULT_FACILITY macro
author: windows-sdk-content
description: Extracts the facility of the specified HRESULT.
old-location: com\hresult_facility_macro.htm
old-project: com
ms.assetid: 35beb1ed-9b63-4e44-a0ae-adaf561e6fd8
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: HRESULT_FACILITY, HRESULT_FACILITY macro [COM], _com_HRESULT_FACILITY, com.hresult_facility, com.hresult_facility_macro, winerror/HRESULT_FACILITY
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
-	HRESULT_FACILITY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# HRESULT_FACILITY macro


## -description


Extracts the facility of the specified <b>HRESULT</b>.


## -parameters




### -param hr

The <b>HRESULT</b> value.


## -remarks



This macro is defined as follows:

<pre class="syntax" xml:space="preserve"><code>#define HRESULT_FACILITY(hr)  (((hr) &gt;&gt; 16) &amp; 0x1fff)</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff544310">Error Handling</a>
 

 

