---
UID: NF:winerror.HRESULT_SEVERITY
title: HRESULT_SEVERITY macro
author: windows-sdk-content
description: Extracts the severity field of the specified HRESULT.
old-location: com\hresult_severity_macro.htm
old-project: com
ms.assetid: e574ddc2-e950-4618-bc16-1b99989a4a68
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: HRESULT_SEVERITY, HRESULT_SEVERITY macro [COM], _com_HRESULT_SEVERITY, com.hresult_severity, com.hresult_severity_macro, winerror/HRESULT_SEVERITY
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
 - HRESULT_SEVERITY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# HRESULT_SEVERITY macro


## -description


Extracts the severity field of the specified <b>HRESULT</b>.


## -parameters




### -param hr

The <b>HRESULT</b>.


## -remarks



This macro is defined as follows:

<pre class="syntax" xml:space="preserve"><code>#define HRESULT_SEVERITY(hr)  (((hr) &gt;&gt; 31) &amp; 0x1)</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff544310">Error Handling</a>
 

 

