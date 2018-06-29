---
UID: NF:winerror.IS_ERROR
title: IS_ERROR macro
author: windows-sdk-content
description: Provides a generic test for errors on any status value.
old-location: com\is_error_macro.htm
old-project: com
ms.assetid: 74497f4b-1c88-4c8a-b9e7-606e77364f48
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: IS_ERROR, IS_ERROR macro [COM], _com_IS_ERROR, com.is_error, com.is_error_macro, winerror/IS_ERROR
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
 - IS_ERROR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IS_ERROR macro


## -description


Provides a generic test for errors on any status value.




## -parameters




### -param Status

The status code. This value can be an <b>HRESULT</b> or an <b>SCODE</b>.


## -remarks



This macro is defined as follows:

<pre class="syntax" xml:space="preserve"><code>#define SEVERITY_ERROR     1
#define IS_ERROR(Status) (((unsigned long)(Status)) &gt;&gt; 31 == SEVERITY_ERROR)</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff544310">Error Handling</a>
 

 

