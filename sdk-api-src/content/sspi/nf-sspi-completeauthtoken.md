---
UID: NF:sspi.CompleteAuthToken
title: CompleteAuthToken function
author: windows-sdk-content
description: Completes an authentication token.
old-location: security\completeauthtoken.htm
tech.root: secauthn
ms.assetid: a404d0a3-d1ea-4708-87d7-2d216e9a5f5f
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: CompleteAuthToken, CompleteAuthToken function [Security], _ssp_completeauthtoken, security.completeauthtoken, sspi/CompleteAuthToken
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: sspi.h
req.include-header: Security.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Secur32.lib
req.dll: Secur32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Secur32.dll
api_name:
 - CompleteAuthToken
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CompleteAuthToken function


## -description


The <b>CompleteAuthToken</b> function completes an authentication token. This function is used by protocols, such as DCE, that need to revise the security information after the transport application has updated some message parameters.
			

This function is supported only by the Digest <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security support provider</a> (SSP).

<b>CompleteAuthToken</b> is used on the server side only.


## -parameters




### -param phContext [in]

A handle of the context that needs to be completed.


### -param pToken [in]

A pointer to a 
<a href="https://msdn.microsoft.com/fc6ef09c-3ba9-4bcb-a3c2-07422af8eaa9">SecBufferDesc</a> structure that contains the buffer descriptor for the entire message.


## -returns



If the function succeeds, the function returns SEC_E_OK.
						

If the function fails, it returns one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle that was passed to the function is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INVALID_TOKEN</b></dt>
</dl>
</td>
<td width="60%">
The token that was passed to the function is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_OUT_OF_SEQUENCE</b></dt>
</dl>
</td>
<td width="60%">
The client's security context was located, but the message number is incorrect. This return value is used with the Digest SSP.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_MESSAGE_ALTERED</b></dt>
</dl>
</td>
<td width="60%">
The client's security context was located, but the client's message has been tampered with. This return value is used with the Digest SSP.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INTERNAL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred that did not map to an SSPI error code.

</td>
</tr>
</table>
 




## -remarks



The client of a transport application calls the <b>CompleteAuthToken</b> function to allow the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> to update a checksum or similar operation after all the protocol headers have been updated by the transport application. The client calls this function only if the 
<a href="https://msdn.microsoft.com/4b482dcc-3878-4bc6-85e4-229a1726cecc">InitializeSecurityContext (Digest)</a> call returned SEC_I_COMPLETE_NEEDED or SEC_I_COMPLETE_AND_CONTINUE.




## -see-also




<a href="https://msdn.microsoft.com/4b482dcc-3878-4bc6-85e4-229a1726cecc">InitializeSecurityContext (Digest)</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374731(v=VS.85).aspx">SSPI Functions</a>



<a href="https://msdn.microsoft.com/fc6ef09c-3ba9-4bcb-a3c2-07422af8eaa9">SecBufferDesc</a>
 

 

