---
UID: NF:winerror.HRESULT_SEVERITY
title: HRESULT_SEVERITY macro
author: windows-sdk-content
description: Extracts the severity field of the specified HRESULT.
old-location: com\hresult_severity_macro.htm
tech.root: com
ms.assetid: e574ddc2-e950-4618-bc16-1b99989a4a68
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: HRESULT_SEVERITY, HRESULT_SEVERITY macro [COM], _com_HRESULT_SEVERITY, com.hresult_severity, com.hresult_severity_macro, winerror/HRESULT_SEVERITY
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
 - HRESULT_SEVERITY
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling</a>
 

 

