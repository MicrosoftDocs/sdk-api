---
UID: NF:sspi.EncryptMessage
title: EncryptMessage function
author: windows-sdk-content
description: Encrypts a message to provide privacy by using Digest.
old-location: security\encryptmessage__digest_.htm
tech.root: secauthn
ms.assetid: 0045e931-929b-40c4-a524-5664d2fc5170
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: EncryptMessage, EncryptMessage (Digest), EncryptMessage function [Security], SealMessage [Security], security.encryptmessage__digest_, sspi/EncryptMessage
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
 - sspicli.dll
api_name:
 - EncryptMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EncryptMessage function


## -description


The <b>EncryptMessage (Digest)</b> function encrypts a message to provide <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">privacy</a>. <b>EncryptMessage (Digest)</b> allows the application to choose among <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic algorithms</a> supported by the chosen mechanism. The <b>EncryptMessage (Digest)</b> function uses the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a> referenced by the context handle. Some packages do not have messages to be encrypted or decrypted but rather provide an integrity <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a> that can be checked.

This function is available as a SASL mechanism only.
<div class="alert"><b>Note</b>  <b>EncryptMessage (Digest)</b> and <a href="https://msdn.microsoft.com/46d45f59-33fa-434a-b329-20b6257c9a19">DecryptMessage (Digest)</a> can be called at the same time from two different threads in a single <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">Security Support Provider Interface</a> (SSPI) context if one thread is encrypting and the other is decrypting. If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</div><div> </div>

## -parameters




### -param phContext [in]

A handle to the security <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">context</a> to be used to encrypt the message.


### -param fQOP [in]

Package-specific flags that indicate the quality of protection. A <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> can use this parameter to enable the selection of cryptographic algorithms.

When using the Digest SSP, this parameter must be set to zero.


### -param pMessage [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/fc6ef09c-3ba9-4bcb-a3c2-07422af8eaa9">SecBufferDesc</a> structure. On input, the structure references one or more 
<a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a> structures that can be of type SECBUFFER_DATA. That buffer contains the message to be encrypted. The  message is encrypted in place, overwriting the original contents of the structure.

The function does not process buffers with the SECBUFFER_READONLY attribute.

The length of the 
<a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a> structure that contains the message must be no greater than <b>cbMaximumMessage</b>, which is obtained from the 
<a href="https://msdn.microsoft.com/d4cd2cc4-77a2-42ba-9029-f4d92706c5c2">QueryContextAttributes (Digest)</a> (SECPKG_ATTR_STREAM_SIZES) function.

When using the Digest SSP,  there must be a second buffer of type SECBUFFER_PADDING or SEC_BUFFER_DATA to hold <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">signature</a> information. To get the size of the output buffer, call the 
<a href="https://msdn.microsoft.com/d4cd2cc4-77a2-42ba-9029-f4d92706c5c2">QueryContextAttributes (Digest)</a> function and specify SECPKG_ATTR_SIZES. The function will return a 
<a href="https://msdn.microsoft.com/46b6a155-8855-4aa0-a513-aa5b3760fcd4">SecPkgContext_Sizes</a> structure. The size of the output buffer is the sum of the values in the <b>cbMaxSignature</b> and <b>cbBlockSize</b> members.

Applications that do not use SSL must supply a <a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a> of type SECBUFFER_PADDING.


### -param MessageSeqNo [in]

The sequence number that the transport application assigned to the message. If the transport application does not maintain sequence numbers, this parameter must be zero.

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
<dt><b>SEC_E_BUFFER_TOO_SMALL</b></dt>
</dl>
</td>
<td width="60%">
The output buffer is too small. For more information, see Remarks.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_CONTEXT_EXPIRED</b></dt>
</dl>
</td>
<td width="60%">
The application is referencing a context that has already been closed. A properly written application should not receive this error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_CRYPTO_SYSTEM_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cipher</a> chosen for the security context is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INSUFFICIENT_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available to complete the requested action.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
A context handle that is not valid was specified in the <i>phContext</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INVALID_TOKEN</b></dt>
</dl>
</td>
<td width="60%">
No SECBUFFER_DATA type buffer was found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_QOP_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Neither confidentiality nor <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">integrity</a> are supported by the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a>.

</td>
</tr>
</table>
 




## -remarks



The <b>EncryptMessage (Digest)</b> function encrypts a message based on the message and the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">session key</a> from a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a>.

If the transport application created the security context to support sequence detection and the caller provides a sequence number, the function includes this information with the encrypted message. Including this information protects against replay, insertion, and suppression of messages. The <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> incorporates the sequence number passed down from the transport application.

When you use the Digest SSP, get the size of the output buffer by calling the <a href="https://msdn.microsoft.com/d4cd2cc4-77a2-42ba-9029-f4d92706c5c2">QueryContextAttributes (Digest)</a> function and specifying SECPKG_ATTR_SIZES. The function will return a <a href="https://msdn.microsoft.com/46b6a155-8855-4aa0-a513-aa5b3760fcd4">SecPkgContext_Sizes</a> structure. The size of the output buffer is the sum of the values in the <b>cbMaxSignature</b> and <b>cbBlockSize</b> members.

<div class="alert"><b>Note</b>  These buffers must be supplied in the order shown.</div>
<div> </div>
<table>
<tr>
<th>Buffer type</th>
<th>Description</th>
</tr>
<tr>
<td>
SECBUFFER_STREAM_HEADER

</td>
<td>
Used internally. No initialization required.

</td>
</tr>
<tr>
<td>
SECBUFFER_DATA

</td>
<td>
Contains the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">plaintext</a> message to be encrypted.

</td>
</tr>
<tr>
<td>
SECBUFFER_STREAM_TRAILER

</td>
<td>
Used internally. No initialization required.

</td>
</tr>
<tr>
<td>
SECBUFFER_EMPTY

</td>
<td>
Used internally. No initialization required. Size can be zero.

</td>
</tr>
</table>
 

For optimal performance, the <i>pMessage</i> structures should be allocated from contiguous memory.

<b>Windows XP:  </b>This function was also known as <b>SealMessage</b>. Applications should now use <b>EncryptMessage (Digest)</b>  only.




## -see-also




<a href="https://msdn.microsoft.com/017683e3-b21a-4e97-9232-582ac7dbd5b2">AcceptSecurityContext (Digest)</a>



<a href="https://msdn.microsoft.com/46d45f59-33fa-434a-b329-20b6257c9a19">DecryptMessage (Digest)</a>



<a href="https://msdn.microsoft.com/4b482dcc-3878-4bc6-85e4-229a1726cecc">InitializeSecurityContext (Digest)</a>



<a href="https://msdn.microsoft.com/d4cd2cc4-77a2-42ba-9029-f4d92706c5c2">QueryContextAttributes (Digest)</a>



<a href="authentication_functions.htm">SSPI Functions</a>



<a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a>



<a href="https://msdn.microsoft.com/fc6ef09c-3ba9-4bcb-a3c2-07422af8eaa9">SecBufferDesc</a>
 

 

