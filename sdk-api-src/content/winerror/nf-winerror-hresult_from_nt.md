---
UID: NF:winerror.HRESULT_FROM_NT
title: HRESULT_FROM_NT macro
author: windows-sdk-content
description: Maps an NT status value to an HRESULT value.
old-location: com\hresult_from_nt_macro.htm
tech.root: com
ms.assetid: e8bf07b8-6bc4-4a6a-b982-03b6436ca6b0
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: HRESULT_FROM_NT, HRESULT_FROM_NT macro [COM], _com_HRESULT_FROM_NT, com.hresult_from_nt, com.hresult_from_nt_macro, winerror/HRESULT_FROM_NT
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
 - HRESULT_FROM_NT
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# HRESULT_FROM_NT macro


## -description


Maps an NT status value to an <b>HRESULT</b> value.


## -parameters




### -param x

The NT status value.


## -remarks



This macro is defined as follows:

<pre class="syntax" xml:space="preserve"><code>#define HRESULT_FROM_NT(x)      ((HRESULT) ((x) | FACILITY_NT_BIT))</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling</a>
 

 

