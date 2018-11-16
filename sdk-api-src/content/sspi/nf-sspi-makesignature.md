---
UID: NF:sspi.MakeSignature
title: MakeSignature function
author: windows-sdk-content
description: Generates a cryptographic checksum of the message, and also includes sequencing information to prevent message loss or insertion.
old-location: security\makesignature.htm
tech.root: SecAuthN
ms.assetid: d17824b0-6121-48a3-b19b-d4fae3e1348e
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 0, 1, 2, 3, 4, MakeSignature, MakeSignature function [Security], _ssp_makesignature, security.makesignature, sspi/MakeSignature
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
 - MakeSignature
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- MakeSignature
: 
---

# MakeSignature function


## -description


The <b>MakeSignature</b> function generates a cryptographic checksum of the message, and also includes sequencing information to prevent message loss or insertion. <b>MakeSignature</b> allows the application to choose between several cryptographic algorithms, if supported by the chosen mechanism. The <b>MakeSignature</b> function uses the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a> referenced by the context handle.

This function is not supported by the Schannel <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security support provider</a> (SSP).


## -parameters




### -param phContext [in]

A handle to the security context to use to sign the message.


### -param fQOP [in]

<a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">Package</a>-specific flags that indicate the quality of protection. A security package can use this parameter to enable the selection of cryptographic algorithms.

When using the Digest SSP, this parameter must be set to zero.


### -param pMessage [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/fc6ef09c-3ba9-4bcb-a3c2-07422af8eaa9">SecBufferDesc</a> structure. On input, the structure references one or more 
<a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a> structures that contain the message to be signed. The function does not process buffers with the SECBUFFER_READONLY_WITH_CHECKSUM  attribute.

The <a href="https://msdn.microsoft.com/fc6ef09c-3ba9-4bcb-a3c2-07422af8eaa9">SecBufferDesc</a> structure also references a <a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a> structure of type SECBUFFER_TOKEN that receives the signature.

When the Digest SSP is used as an HTTP authentication protocol, the buffers should be configured as follows.

<table>
<tr>
<th>Buffer #/buffer type</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
<dt>SECBUFFER_TOKEN</dt>
</dl>
</td>
<td width="60%">
Empty.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
<dt>SECBUFFER_PKG_PARAMS</dt>
</dl>
</td>
<td width="60%">
Method.

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
<dt>SECBUFFER_PKG_PARAMS</dt>
</dl>
</td>
<td width="60%">
URL.

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
<dt>SECBUFFER_PKG_PARAMS</dt>
</dl>
</td>
<td width="60%">
HEntity. For more information, see 
<a href="https://msdn.microsoft.com/0df02be2-f42e-46d0-a206-765adf3d7a72">Input Buffers for the Digest Challenge Response</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="4"></a><dl>
<dt><b>4</b></dt>
<dt>SECBUFFER_PADDING</dt>
</dl>
</td>
<td width="60%">
Empty. Receives the <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">signature</a>.

</td>
</tr>
</table>
 

When the Digest SSP is used as an SASL mechanism, the buffers should be configured as follows.

<table>
<tr>
<th>Buffer #/buffer type</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
<dt>SECBUFFER_TOKEN</dt>
</dl>
</td>
<td width="60%">
Empty. Receives the signature. This buffer must be large enough to hold the largest possible signature. Determine the size required by calling the 
<a href="https://msdn.microsoft.com/67bc087f-7519-4c8a-9b34-b3ecd306a334">QueryContextAttributes (General)</a> function and specifying SECPKG_ATTR_SIZES. Check the returned 
<a href="https://msdn.microsoft.com/46b6a155-8855-4aa0-a513-aa5b3760fcd4">SecPkgContext_Sizes</a> structure member <b>cbMaxSignature</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
<dt>SECBUFFER_DATA</dt>
</dl>
</td>
<td width="60%">
Message to be signed.

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
<dt>SECBUFFER_PADDING</dt>
</dl>
</td>
<td width="60%">
Empty.

</td>
</tr>
</table>
 


### -param MessageSeqNo [in]

The sequence number that the transport application assigned to the message. If the transport application does not maintain sequence numbers, this parameter is zero.

When using the Digest SSP, this parameter must be set to zero. The Digest SSP manages sequence numbering internally.


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
<dt><b>SEC_I_RENEGOTIATE</b></dt>
</dl>
</td>
<td width="60%">
The remote party requires a new handshake sequence or the application has just initiated a shutdown. Return to the negotiation loop and call 
<a href="https://msdn.microsoft.com/eaa15fed-4438-4e43-9be3-aa100ca453c7">AcceptSecurityContext (General)</a> or 
<a href="https://msdn.microsoft.com/21d965d4-3c03-4e29-a70d-4538c5c366b0">InitializeSecurityContext (General)</a> again. An empty input buffer is passed in the first call.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The context handle specified by <i>phContext</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INVALID_TOKEN</b></dt>
</dl>
</td>
<td width="60%">
<i>pMessage</i> did not contain a valid SECBUFFER_TOKEN buffer or contained too few buffers.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_OUT_OF_SEQUENCE</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/28d229ef-53ce-4d17-aba0-3bbf51e3ff0c">nonce</a> count is out of sequence.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_NO_AUTHENTICATING_AUTHORITY</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a> (<i>phContext</i>) must be revalidated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The nonce count is not numeric.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_QOP_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The quality of protection negotiated between the client and server did not include <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">integrity</a> checking.

</td>
</tr>
</table>
 




## -remarks



The <b>MakeSignature</b> function generates a signature that is based on the message and the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">session key</a> for the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">context</a>.

The <a href="https://msdn.microsoft.com/bebeef92-1d6e-4879-846f-12d706db0653">VerifySignature</a> function verifies the messages signed by the <b>MakeSignature</b> function.

If the transport application created the security context to support sequence detection and the caller provides a sequence number, the function includes this information in the signature. This protects against reply, insertion, and suppression of messages. The <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> incorporates the sequence number passed down from the transport application.




## -see-also




<a href="authentication_functions.htm">SSPI Functions</a>



<a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a>



<a href="https://msdn.microsoft.com/fc6ef09c-3ba9-4bcb-a3c2-07422af8eaa9">SecBufferDesc</a>



<a href="https://msdn.microsoft.com/bebeef92-1d6e-4879-846f-12d706db0653">VerifySignature</a>
 

 

