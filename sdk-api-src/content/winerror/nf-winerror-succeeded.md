---
UID: NF:winerror.SUCCEEDED
title: SUCCEEDED macro
author: windows-sdk-content
description: Provides a generic test for success on any status value.
old-location: com\succeeded_macro.htm
tech.root: com
ms.assetid: 7a258b0b-d214-46c5-be0a-6493cd14a0e5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SUCCEEDED, SUCCEEDED macro [COM], _com_SUCCEEDED, com.succeeded, com.succeeded_macro, winerror/SUCCEEDED
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
 - SUCCEEDED
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SUCCEEDED macro


## -description


Provides a generic test for success on any status value.


## -parameters




### -param hr

The status code. This value can be an <b>HRESULT</b> or an <b>SCODE</b>. A non-negative number indicates success.



## -remarks



This macro is defined as follows:

<pre class="syntax" xml:space="preserve"><code>#define SUCCEEDED(hr) (((HRESULT)(hr)) &gt;= 0)</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling</a>
 

 

