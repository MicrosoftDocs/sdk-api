---
UID: NF:sspi.DecryptMessage
title: DecryptMessage function
author: windows-sdk-content
description: Decrypts a message by using Digest.
old-location: security\decryptmessage__digest_.htm
tech.root: SecAuthN
ms.assetid: 46d45f59-33fa-434a-b329-20b6257c9a19
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: DecryptMessage, DecryptMessage (Digest), DecryptMessage function [Security], SECQOP_WRAP_NO_ENCRYPT, SIGN_ONLY, UnsealMessage [Security], security.decryptmessage__digest_, sspi/DecryptMessage
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
 - DecryptMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DecryptMessage function


## -description


The <b>DecryptMessage (Digest)</b> function decrypts a message. Some packages do not encrypt and decrypt messages but rather perform and check an integrity <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a>.

The Digest <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security support provider</a> (SSP) provides encryption and decryption confidentiality for messages exchanged between client and server as a SASL mechanism only.
<div class="alert"><b>Note</b>  <a href="https://msdn.microsoft.com/0045e931-929b-40c4-a524-5664d2fc5170">EncryptMessage (Digest)</a> and <b>DecryptMessage (Digest)</b> can be called at the same time from two different threads in a single <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">Security Support Provider Interface</a> (SSPI) context if one thread is encrypting and the other is decrypting. If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</div><div> </div>

## -parameters




### -param phContext [in]

A handle to the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a> to be used to decrypt the message.


### -param pMessage [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/fc6ef09c-3ba9-4bcb-a3c2-07422af8eaa9">SecBufferDesc</a> structure. On input, the structure references one or more 
<a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a> structures. At least one of these must be of type SECBUFFER_DATA. That buffer contains the encrypted message. The encrypted message is decrypted in place, overwriting the original contents of its buffer.

When using the Digest SSP, on input, the structure references one or more 
<a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a> structures. One of these must be of type SECBUFFER_DATA or SECBUFFER_STREAM, and it must contain the encrypted message.


### -param MessageSeqNo [in]

The sequence number expected by the transport application, if any. If the transport application does not maintain sequence numbers, this parameter must be set to zero.

When using the Digest SSP, this parameter must be set to zero. The Digest SSP manages sequence numbering internally.


### -param pfQOP [out]

A pointer to a variable of type <b>ULONG</b> that receives package-specific flags that indicate the quality of protection.
						

This parameter can be one of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SECQOP_WRAP_NO_ENCRYPT"></a><a id="secqop_wrap_no_encrypt"></a><dl>
<dt><b>SECQOP_WRAP_NO_ENCRYPT</b></dt>
</dl>
</td>
<td width="60%">
The message was not encrypted, but a header or trailer was produced.

<div class="alert"><b>Note</b>  KERB_WRAP_NO_ENCRYPT has the same value and the same meaning.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="SIGN_ONLY_"></a><a id="sign_only_"></a><dl>
<dt><b>SIGN_ONLY </b></dt>
</dl>
</td>
<td width="60%">
When using the Digest SSP, use this flag when the security context is set to verify the <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">signature</a> only. For more information, see 
<a href="https://msdn.microsoft.com/bee4236c-69e5-4281-a6b3-be316bac0a11">Quality of Protection</a>.

</td>
</tr>
</table>
 


## -returns



If the function verifies that the message was received in the correct sequence, the function returns SEC_E_OK.

If the function fails to decrypt the message, it returns one of the following error codes.

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
The message buffer is too small.  Used with the Digest SSP.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_CRYPTO_SYSTEM_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The cipher chosen for the security context is not supported. Used with the Digest SSP.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INCOMPLETE_MESSAGE</b></dt>
</dl>
</td>
<td width="60%">
The data in the input buffer is incomplete. The application needs to read more data from the server and call <a href="https://msdn.microsoft.com/46d45f59-33fa-434a-b329-20b6257c9a19">DecryptMessage (Digest)</a> again.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
A context handle that is not valid was specified in the <i>phContext</i> parameter. Used with the Digest SSP.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_MESSAGE_ALTERED</b></dt>
</dl>
</td>
<td width="60%">
The message has been altered. Used with the Digest SSP.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_OUT_OF_SEQUENCE</b></dt>
</dl>
</td>
<td width="60%">
The message was not received in the correct sequence.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_QOP_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Neither confidentiality nor <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">integrity</a> are supported by the security context. Used with the Digest SSP.

</td>
</tr>
</table>
 




## -remarks



Sometimes an application will read data from the remote party, attempt to decrypt it by using <b>DecryptMessage (Digest)</b>, and discover that <b>DecryptMessage (Digest)</b> succeeded but the output buffers are empty. This is normal behavior, and applications must be able to deal with it.

<b>Windows XP:  </b>This function was also known as <b>UnsealMessage</b>. Applications should now use <b>DecryptMessage (Digest)</b> only.




## -see-also




<a href="https://msdn.microsoft.com/0045e931-929b-40c4-a524-5664d2fc5170">EncryptMessage (Digest)</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374731(v=VS.85).aspx">SSPI Functions</a>



<a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a>



<a href="https://msdn.microsoft.com/fc6ef09c-3ba9-4bcb-a3c2-07422af8eaa9">SecBufferDesc</a>
 

 

