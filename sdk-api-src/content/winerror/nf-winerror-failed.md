---
UID: NF:winerror.FAILED
title: FAILED macro
author: windows-sdk-content
description: Provides a generic test for failure on any status value.
old-location: com\failed_macro.htm
old-project: com
ms.assetid: d9c4ff73-c255-4a82-b901-23bd5b41ee6c
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: FAILED, FAILED macro [COM], _com_FAILED, com.failed, com.failed_macro, winerror/FAILED
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
 - FAILED
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# FAILED macro


## -description


Provides a generic test for failure on any status value. 


## -parameters




### -param hr

The status code. This value can be an <b>HRESULT</b> or an <b>SCODE</b>. A negative number indicates failure.


## -remarks



This macro is defined as follows:

<pre class="syntax" xml:space="preserve"><code>#define FAILED(hr) (((HRESULT)(hr)) &lt; 0)</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff544310">Error Handling</a>
 

 

