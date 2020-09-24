---
UID: NF:sspi.EncryptMessage
title: EncryptMessage function (sspi.h)
description: Encrypts a message to provide privacy by using Digest.
helpviewer_keywords: ["EncryptMessage","EncryptMessage (Digest)","EncryptMessage function [Security]","SealMessage [Security]","security.encryptmessage__digest_","sspi/EncryptMessage"]
old-location: security\encryptmessage__digest_.htm
tech.root: security
ms.assetid: 0045e931-929b-40c4-a524-5664d2fc5170
ms.date: 12/05/2018
ms.keywords: EncryptMessage, EncryptMessage (Digest), EncryptMessage function [Security], SealMessage [Security], security.encryptmessage__digest_, sspi/EncryptMessage
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EncryptMessage
 - sspi/EncryptMessage
dev_langs:
 - c++
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
---

# EncryptMessage function


## -description

The <b>EncryptMessage (Digest)</b> function encrypts a message to provide <a href="/windows/desktop/SecGloss/p-gly">privacy</a>. <b>EncryptMessage (Digest)</b> allows the application to choose among <a href="/windows/desktop/SecGloss/c-gly">cryptographic algorithms</a> supported by the chosen mechanism. The <b>EncryptMessage (Digest)</b> function uses the <a href="/windows/desktop/SecGloss/s-gly">security context</a> referenced by the context handle. Some packages do not have messages to be encrypted or decrypted but rather provide an integrity <a href="/windows/desktop/SecGloss/h-gly">hash</a> that can be checked.

This function is available as a SASL mechanism only.
<div class="alert"><b>Note</b>  <b>EncryptMessage (Digest)</b> and <a href="/windows/desktop/api/sspi/nf-sspi-decryptmessage">DecryptMessage (Digest)</a> can be called at the same time from two different threads in a single <a href="/windows/desktop/SecGloss/s-gly">Security Support Provider Interface</a> (SSPI) context if one thread is encrypting and the other is decrypting. If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</div><div> </div>

## -parameters

### -param phContext [in]

A handle to the security <a href="/windows/desktop/SecGloss/c-gly">context</a> to be used to encrypt the message.

### -param fQOP [in]

Package-specific flags that indicate the quality of protection. A <a href="/windows/desktop/SecGloss/s-gly">security package</a> can use this parameter to enable the selection of cryptographic algorithms.

When using the Digest SSP, this parameter must be set to zero.

### -param pMessage [in, out]

A pointer to a 
<a href="/windows/desktop/api/sspi/ns-sspi-secbufferdesc">SecBufferDesc</a> structure. On input, the structure references one or more 
<a href="/windows/desktop/api/sspi/ns-sspi-secbuffer">SecBuffer</a> structures that can be of type SECBUFFER_DATA. That buffer contains the message to be encrypted. The  message is encrypted in place, overwriting the original contents of the structure.

The function does not process buffers with the SECBUFFER_READONLY attribute.

The length of the 
<a href="/windows/desktop/api/sspi/ns-sspi-secbuffer">SecBuffer</a> structure that contains the message must be no greater than <b>cbMaximumMessage</b>, which is obtained from the 
<a href="/windows/desktop/api/rrascfg/nn-rrascfg-ieapproviderconfig">QueryContextAttributes (Digest)</a> (SECPKG_ATTR_STREAM_SIZES) function.

When using the Digest SSP,  there must be a second buffer of type SECBUFFER_PADDING or SEC_BUFFER_DATA to hold <a href="/windows/desktop/SecGloss/d-gly">signature</a> information. To get the size of the output buffer, call the 
<a href="/windows/desktop/api/rrascfg/nn-rrascfg-ieapproviderconfig">QueryContextAttributes (Digest)</a> function and specify SECPKG_ATTR_SIZES. The function will return a 
<a href="/windows/desktop/api/sspi/ns-sspi-secpkgcontext_sizes">SecPkgContext_Sizes</a> structure. The size of the output buffer is the sum of the values in the <b>cbMaxSignature</b> and <b>cbBlockSize</b> members.

Applications that do not use SSL must supply a <a href="/windows/desktop/api/sspi/ns-sspi-secbuffer">SecBuffer</a> of type SECBUFFER_PADDING.

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
The <a href="/windows/desktop/SecGloss/c-gly">cipher</a> chosen for the security context is not supported.

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
Neither confidentiality nor <a href="/windows/desktop/SecGloss/i-gly">integrity</a> are supported by the <a href="/windows/desktop/SecGloss/s-gly">security context</a>.

</td>
</tr>
</table>

## -remarks

The <b>EncryptMessage (Digest)</b> function encrypts a message based on the message and the <a href="/windows/desktop/SecGloss/s-gly">session key</a> from a <a href="/windows/desktop/SecGloss/s-gly">security context</a>.

If the transport application created the security context to support sequence detection and the caller provides a sequence number, the function includes this information with the encrypted message. Including this information protects against replay, insertion, and suppression of messages. The <a href="/windows/desktop/SecGloss/s-gly">security package</a> incorporates the sequence number passed down from the transport application.

When you use the Digest SSP, get the size of the output buffer by calling the <a href="/windows/desktop/api/rrascfg/nn-rrascfg-ieapproviderconfig">QueryContextAttributes (Digest)</a> function and specifying SECPKG_ATTR_SIZES. The function will return a <a href="/windows/desktop/api/sspi/ns-sspi-secpkgcontext_sizes">SecPkgContext_Sizes</a> structure. The size of the output buffer is the sum of the values in the <b>cbMaxSignature</b> and <b>cbBlockSize</b> members.

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
Contains the <a href="/windows/desktop/SecGloss/p-gly">plaintext</a> message to be encrypted.

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

<a href="/windows/desktop/api/sspi/nf-sspi-acceptsecuritycontext">AcceptSecurityContext (Digest)</a>



<a href="/windows/desktop/api/sspi/nf-sspi-decryptmessage">DecryptMessage (Digest)</a>



<a href="/windows/desktop/api/sspi/nf-sspi-initializesecuritycontexta">InitializeSecurityContext (Digest)</a>



<a href="/windows/desktop/api/rrascfg/nn-rrascfg-ieapproviderconfig">QueryContextAttributes (Digest)</a>



<a href="/windows/desktop/SecAuthN/authentication-functions">SSPI Functions</a>



<a href="/windows/desktop/api/sspi/ns-sspi-secbuffer">SecBuffer</a>



<a href="/windows/desktop/api/sspi/ns-sspi-secbufferdesc">SecBufferDesc</a>