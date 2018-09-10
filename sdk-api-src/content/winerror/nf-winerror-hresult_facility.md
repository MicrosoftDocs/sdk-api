---
UID: NF:winerror.HRESULT_FACILITY
title: HRESULT_FACILITY macro
author: windows-sdk-content
description: Extracts the facility of the specified HRESULT.
old-location: com\hresult_facility_macro.htm
tech.root: com
ms.assetid: 35beb1ed-9b63-4e44-a0ae-adaf561e6fd8
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: HRESULT_FACILITY, HRESULT_FACILITY macro [COM], _com_HRESULT_FACILITY, com.hresult_facility, com.hresult_facility_macro, winerror/HRESULT_FACILITY
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
 - HRESULT_FACILITY
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling</a>
 

 

