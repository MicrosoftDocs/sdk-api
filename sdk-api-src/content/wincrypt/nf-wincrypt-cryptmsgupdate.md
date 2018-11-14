---
UID: NF:wincrypt.CryptMsgUpdate
title: CryptMsgUpdate function
author: windows-sdk-content
description: Adds contents to a cryptographic message.
old-location: security\cryptmsgupdate.htm
tech.root: seccrypto
ms.assetid: d27d75f0-1646-4926-b375-59e52b00326c
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: CryptMsgUpdate, CryptMsgUpdate function [Security], _crypto2_cryptmsgupdate, security.cryptmsgupdate, wincrypt/CryptMsgUpdate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptMsgUpdate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CryptMsgUpdate
: 
---

# CryptMsgUpdate function


## -description


The <b>CryptMsgUpdate</b> function adds contents to a cryptographic message. The use of this function allows messages to be constructed piece by piece through repetitive calls of <b>CryptMsgUpdate</b>. The added message content is either encoded or decoded depending on whether the message was opened with 
<a href="https://msdn.microsoft.com/b0d2610b-05ba-4fb6-8f38-10f970a52091">CryptMsgOpenToEncode</a> or 
<a href="https://msdn.microsoft.com/b3df6312-c866-4faa-8b89-bda67c697631">CryptMsgOpenToDecode</a>.


## -parameters




### -param hCryptMsg [in]

Cryptographic message handle of the message to be updated.


### -param pbData [in]

A pointer to the buffer holding the data to be encoded or decoded.


### -param cbData [in]

Number of bytes of data in the <i>pbData</i> buffer.


### -param fFinal [in]

Indicates that the last block of data for encoding or decoding is being processed. Correct usage of this flag is dependent upon whether the message being processed has detached data. The inclusion of detached data in a message is indicated by setting <i>dwFlags</i> to CMSG_DETACHED_FLAG in the call to the function that opened the message. 




If CMSG_DETACHED_FLAG was not set and the message was opened using either 
<a href="https://msdn.microsoft.com/b3df6312-c866-4faa-8b89-bda67c697631">CryptMsgOpenToDecode</a> or 
<a href="https://msdn.microsoft.com/b0d2610b-05ba-4fb6-8f38-10f970a52091">CryptMsgOpenToEncode</a>, <i>fFinal</i> is set to <b>TRUE</b>, and <b>CryptMsgUpdate</b> is only called once.

If the CMSG_DETACHED_FLAG flag was set and a message is opened using <a href="https://msdn.microsoft.com/b0d2610b-05ba-4fb6-8f38-10f970a52091">CryptMsgOpenToEncode</a>, <i>fFinal</i> is set to <b>TRUE</b> only on the last call to <b>CryptMsgUpdate</b>.

If the CMSG_DETACHED_FLAG flag was set and a message is opened using <a href="https://msdn.microsoft.com/b3df6312-c866-4faa-8b89-bda67c697631">CryptMsgOpenToDecode</a>, <i>fFinal</i> is set to <b>TRUE</b> when the header is processed by a single call to <b>CryptMsgUpdate</b>. It is set to <b>FALSE</b> while processing the detached data in subsequent calls to <b>CryptMsgUpdate</b> until the last detached data block is to be processed. On the last call to <b>CryptMsgUpdate</b>, it is set to <b>TRUE</b>.

When detached data is decoded, the header and the content of a message are contained in different BLOBs. Each BLOB requires that <i>fFinal</i> be set to <b>TRUE</b> when the last call to the function is made for that BLOB.


## -returns



If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

Errors encountered in the application defined callback function specified by <i>pStreamInfo</i> in 
<a href="https://msdn.microsoft.com/b3df6312-c866-4faa-8b89-bda67c697631">CryptMsgOpenToDecode</a> and 
<a href="https://msdn.microsoft.com/b0d2610b-05ba-4fb6-8f38-10f970a52091">CryptMsgOpenToEncode</a> might be propagated to <b>CryptMsgUpdate</b> if streaming is used. If this happens, <a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> is not called by <b>CryptMsgUpdate</b> after the callback function returns, which preserves any errors encountered under the control of the application. It is the responsibility of the callback function (or one of the APIs that it calls) to call <b>SetLastError</b> if an error occurs while the application is processing the streamed data.

The following table lists the error codes most commonly returned by the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_INVALID_MSG_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The message type is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_MSG_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error was encountered doing a cryptographic operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_OID_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The object identifier is badly formatted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_UNEXPECTED_ENCODING</b></dt>
</dl>
</td>
<td width="60%">
The message is not encoded as expected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_UNKNOWN_ALGO</b></dt>
</dl>
</td>
<td width="60%">
The cryptographic algorithm is unknown.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Ran out of memory.

</td>
</tr>
</table>
 

Propagated errors might be encountered from any of the following functions:<ul>
<li>
<a href="https://msdn.microsoft.com/ec1482a2-c2cb-4c5f-af9c-d493134413d6">CryptHashData</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ed008c07-1a40-4075-bdaa-eb7f7e12d9c3">CryptGetHashParam</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9cf0de04-fdad-457d-8137-16d98f915cd5">CryptSignHash</a>
</li>
<li>
<a href="https://msdn.microsoft.com/07956d74-0e22-484b-9bf1-e0184a2ff32f">CryptGetKeyParam</a>
</li>
<li>
<a href="https://msdn.microsoft.com/697c4960-552b-4c3a-95cf-4632af56945b">CryptEncrypt</a>
</li>
<li>
<a href="https://msdn.microsoft.com/05e3db57-8d83-48e2-8590-68039ea27253">CryptCreateHash</a>
</li>
</ul>


If the function fails, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> may return an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="https://msdn.microsoft.com/cb1f34dd-dab4-4ffb-a73b-79a214290509">ASN.1 Encoding/Decoding Return Values</a>. 




## -see-also




<a href="https://msdn.microsoft.com/5a05eb09-208f-4e94-abfa-c2f14c0a3164">CryptMsgGetParam</a>



<a href="https://msdn.microsoft.com/b3df6312-c866-4faa-8b89-bda67c697631">CryptMsgOpenToDecode</a>



<a href="https://msdn.microsoft.com/b0d2610b-05ba-4fb6-8f38-10f970a52091">CryptMsgOpenToEncode</a>



<a href="cryptography_functions.htm">Low-level Message Functions</a>



<a href="cryptography_functions.htm">Simplified Message Functions</a>
 

 

