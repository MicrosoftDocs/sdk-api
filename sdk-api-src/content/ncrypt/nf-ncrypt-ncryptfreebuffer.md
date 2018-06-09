---
UID: NF:ncrypt.NCryptFreeBuffer
title: NCryptFreeBuffer function
author: windows-sdk-content
description: Releases a block of memory allocated by a CNG key storage provider.
old-location: security\ncryptfreebuffer_func.htm
old-project: SecCNG
ms.assetid: 15f19999-cf64-4a30-b38d-9372066add0a
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: NCryptFreeBuffer, NCryptFreeBuffer function [Security], ncrypt/NCryptFreeBuffer, security.ncryptfreebuffer_func
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ncrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
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
req.typenames: SESSION_HEADER, *PSESSION_HEADER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ncrypt.dll
api_name:
 - NCryptFreeBuffer
product: Windows
targetos: Windows
req.lib: Ncrypt.lib
req.dll: Ncrypt.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
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



A service must not call this function from its <a href="http://go.microsoft.com/fwlink/p/?linkid=137250">StartService Function</a>. If a service calls this function from its StartService function, a deadlock can occur, and the service may stop responding.



