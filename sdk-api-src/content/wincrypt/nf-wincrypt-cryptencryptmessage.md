---
UID: NF:wincrypt.CryptEncryptMessage
title: CryptEncryptMessage function
author: windows-sdk-content
description: The CryptEncryptMessage function encrypts and encodes a message.
old-location: security\cryptencryptmessage.htm
tech.root: SecCrypto
ms.assetid: 927f2e9a-96cf-4744-bd57-420b5034d28d
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: CryptEncryptMessage, CryptEncryptMessage function [Security], _crypto2_cryptencryptmessage, security.cryptencryptmessage, wincrypt/CryptEncryptMessage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincrypt.h
req.include-header: 
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
 - CryptEncryptMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptEncryptMessage function


## -description


The <b>CryptEncryptMessage</b> function <a href="https://msdn.microsoft.com/f1caccd2-3453-448e-b194-bf899eff8091">encrypts</a> and <a href="https://msdn.microsoft.com/f1caccd2-3453-448e-b194-bf899eff8091">encodes</a> a message.


## -parameters




### -param pEncryptPara [in]

A pointer to a 
<a href="https://msdn.microsoft.com/c683c515-3061-48e3-a64a-2798bd1245b0">CRYPT_ENCRYPT_MESSAGE_PARA</a> structure that contains the encryption parameters.

The <b>CryptEncryptMessage</b> function does not support the SHA2 OIDs, <b>szOID_DH_SINGLE_PASS_STDDH_SHA256_KDF</b> and  <b>szOID_DH_SINGLE_PASS_STDDH_SHA384_KDF</b>.


### -param cRecipientCert [in]

Number of elements in the <i>rgpRecipientCert</i> array.


### -param rgpRecipientCert [in]

Array of pointers to 
<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structures that contain the certificates of intended recipients of the message.


### -param pbToBeEncrypted [in]

A pointer to a buffer that contains the message that is to be encrypted.


### -param cbToBeEncrypted [in]

The size, in bytes, of the message that is to be encrypted.


### -param pbEncryptedBlob [out]

A pointer to <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> that contains a buffer that receives the encrypted and encoded message. 




To set the size of this information for memory allocation purposes, this parameter can be <b>NULL</b>. For more information, see 
<a href="https://msdn.microsoft.com/ef99edef-39b2-4d78-9c01-13720215d47f">Retrieving Data of Unknown Length</a>.


### -param pcbEncryptedBlob [in, out]

A pointer to a <b>DWORD</b> that specifies the size, in bytes, of the buffer pointed to by the <i>pbEncryptedBlob</i> parameter. When the function returns, this variable contains the size, in bytes, of the encrypted and encoded message copied to <i>pbEncryptedBlob</i>. 




<div class="alert"><b>Note</b>  When processing the data returned in the buffer of the <i>pbEncryptedBlob</i>, applications need to use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data will fit in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

## -returns



If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

<div class="alert"><b>Note</b>  Errors from calls to 
<a href="https://msdn.microsoft.com/b65dd856-2dfa-4cda-9b2f-b32f3c291470">CryptGenKey</a>, 
<a href="https://msdn.microsoft.com/697c4960-552b-4c3a-95cf-4632af56945b">CryptEncrypt</a>, 
<a href="https://msdn.microsoft.com/f48b6ec9-e03b-43b0-9f22-120ae93d934c">CryptImportKey</a>, and 
<a href="https://msdn.microsoft.com/8a7c7b46-3bea-4043-b568-6d91d6335737">CryptExportKey</a> can be propagated to this function.</div>
<div> </div>
The <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function returns the following error codes most often.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
If the buffer specified by the <i>pbEncryptedBlob</i> parameter is not large enough to hold the returned data, the function sets the ERROR_MORE_DATA code and stores the required buffer size, in bytes, in the variable pointed to by <i>pcbEncryptedBlob</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">message encoding type</a> is not valid. Currently only PKCS_7_ASN_ENCODING is supported. The <b>cbSize</b> in *<i>pEncryptPara</i> is not valid.

</td>
</tr>
</table>
 

If the function fails, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> may return an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="https://msdn.microsoft.com/cb1f34dd-dab4-4ffb-a73b-79a214290509">ASN.1 Encoding/Decoding Return Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Simplified Message Functions</a>
 

 

