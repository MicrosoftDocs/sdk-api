---
UID: NF:ncrypt.NCryptFreeBuffer
title: NCryptFreeBuffer function (ncrypt.h)
description: Releases a block of memory allocated by a CNG key storage provider.
old-location: security\ncryptfreebuffer_func.htm
tech.root: SecCNG
ms.assetid: 15f19999-cf64-4a30-b38d-9372066add0a
ms.date: 12/05/2018
ms.keywords: NCryptFreeBuffer, NCryptFreeBuffer function [Security], ncrypt/NCryptFreeBuffer, security.ncryptfreebuffer_func
f1_keywords:
- ncrypt/NCryptFreeBuffer
dev_langs:
- c++
req.header: ncrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ncrypt.lib
req.dll: Ncrypt.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Ncrypt.dll
api_name:
- NCryptFreeBuffer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# NCryptFreeBuffer function


## -description


The <b>NCryptFreeBuffer</b> function releases a block of memory allocated by a CNG key storage provider.


## -parameters




### -param pvInput [in]

The address of the memory to be released.


## -returns



Returns a status code that indicates the success or failure of the function.


Possible return codes include, but are not limited to, the following.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pvInput</i> parameter is not valid.

</td>
</tr>
</table>
 




## -remarks



A service must not call this function from its <a href="https://msdn.microsoft.com/library/ms686321.aspx">StartService Function</a>. If a service calls this function from its StartService function, a deadlock can occur, and the service may stop responding.



