---
UID: NF:bits2_5.IBackgroundCopyJobHttpOptions.GetCustomHeaders
title: IBackgroundCopyJobHttpOptions::GetCustomHeaders
author: windows-sdk-content
description: Retrieves the custom headers set by an earlier call to IBackgroundCopyJobHttpOptions::SetCustomHeaders (that is, headers which BITS will be sending to the remote, not headers which BITS receives from the remote).
old-location: bits\ibackgroundcopyjobhttpoptions_getcustomheaders.htm
old-project: bits
ms.assetid: 8be6e9ec-7c74-44ff-94d7-a1a1d7fb18e9
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetCustomHeaders, GetCustomHeaders method [BITS], GetCustomHeaders method [BITS],IBackgroundCopyJobHttpOptions interface, IBackgroundCopyJobHttpOptions interface [BITS],GetCustomHeaders method, IBackgroundCopyJobHttpOptions.GetCustomHeaders, IBackgroundCopyJobHttpOptions::GetCustomHeaders, bits.ibackgroundcopyjobhttpoptions_getcustomheaders, bits2_5/IBackgroundCopyJobHttpOptions::GetCustomHeaders
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bits2_5.h
req.include-header: Bits.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits2_5.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BG_CERT_STORE_LOCATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBackgroundCopyJobHttpOptions.GetCustomHeaders
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: 
req.irql: 
---

# IBackgroundCopyJobHttpOptions::GetCustomHeaders


## -description


Retrieves the custom headers set by an earlier call to<a href="https://msdn.microsoft.com/en-us/library/Aa964258(v=VS.85).aspx"> IBackgroundCopyJobHttpOptions::SetCustomHeaders</a> (that is, headers which BITS will be sending to the remote, not headers which BITS receives from the remote).


## -parameters




### -param pRequestHeaders [out]

Null-terminated string that contains the custom headers. Each header is terminated by a carriage return and line feed (CR/LF) character. To free the string when finished, call  the 
<a href="https://msdn.microsoft.com/en-us/library/ms680722(v=VS.85).aspx">CoTaskMemFree</a> function.


## -returns



The following table lists some of the possible return values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
Successfully retrieved the headers.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
The job does not specify custom headers.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_ACCESSDENIED</b></b></dt>
</dl>
</td>
<td width="60%">
The user does not have permission to retrieve the custom headers.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>RPC_X_NULL_REF_POINTER</b></b></dt>
</dl>
</td>
<td width="60%">
The <i>pRequestHeaders</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



Only the job owner can retrieve the custom headers. To specify the headers, call the <a href="https://msdn.microsoft.com/en-us/library/Aa964258(v=VS.85).aspx">IBackgroundCopyJobHttpOptions::SetCustomHeaders</a> method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa964250(v=VS.85).aspx">IBackgroundCopyJobHttpOptions</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa964258(v=VS.85).aspx">IBackgroundCopyJobHttpOptions::SetCustomHeaders</a>
 

 

