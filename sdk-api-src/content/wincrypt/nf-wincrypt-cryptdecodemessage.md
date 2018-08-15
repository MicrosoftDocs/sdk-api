---
UID: NF:wincrypt.CryptDecodeMessage
title: CryptDecodeMessage function
author: windows-sdk-content
description: Decodes, decrypts, and verifies a cryptographic message.
old-location: security\cryptdecodemessage.htm
old-project: seccrypto
ms.assetid: 25ffd058-8f75-4ba5-b075-e3efc09f5d9d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CryptDecodeMessage, CryptDecodeMessage function [Security], _crypto2_cryptdecodemessage, security.cryptdecodemessage, wincrypt/CryptDecodeMessage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptDecodeMessage
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CryptDecodeMessage function


## -description


The <b>CryptDecodeMessage</b> function decodes, decrypts, and verifies a cryptographic message.

This function can be used when the type of cryptographic message is unknown. The <i>dwMsgTypeFlags</i> constants can be combined with a bitwise-<b>OR</b> operation so that the function will try to find one of the types. When one of the types is found, the function reports the type found and returns the data appropriate to that type.

In each pass, the function cracks only a single level of encryption or encoding. For additional cracking, this function, or one of the other 
<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Simplified Message Functions</a>, must be called again.


## -parameters




### -param dwMsgTypeFlags [in]

Indicates the message type. Message types can be combined with the bitwise-<b>OR</b> operator. This parameter can be one of the following message types:

<ul>
<li>CMSG_DATA_FLAG</li>
<li>CMSG_SIGNED_FLAG</li>
<li>CMSG_ENVELOPED_FLAG</li>
<li>CMSG_SIGNED_AND_ENVELOPED_FLAG</li>
<li>CMSG_HASHED_FLAG</li>
</ul>
<div class="alert"><b>Note</b>  After return, the <b>DWORD</b> pointed to by <i>pdwMsgType</i> is set with the type of the message.</div>
<div> </div>

### -param pDecryptPara [in]

A pointer to a 
<a href="https://msdn.microsoft.com/67e136cd-12e3-4a31-9d8b-b53e1129e940">CRYPT_DECRYPT_MESSAGE_PARA</a> structure that contains  decryption parameters.


### -param pVerifyPara [in]

A pointer to a 
<a href="https://msdn.microsoft.com/bbd56b5e-2bbe-420f-8842-1be50dca779f">CRYPT_VERIFY_MESSAGE_PARA</a> structure that contains   verification parameters.


### -param dwSignerIndex [in]

Indicates which signer, among the possible many signers of a message, is to be verified. This index can be changed in multiple calls to the function to verify additional signers. 




<i>dwSignerIndex</i> is set to zero for the first signer. If the function returns <b>FALSE</b>, and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns CRYPT_E_NO_SIGNER, the previous call returned the last signer of the message. This parameter is used only with messages of types CMSG_SIGNED_AND_ENVELOPED or CMSG_SIGNED. For all other message types, it should be set to zero.


### -param pbEncodedBlob [in]

A pointer to the encoded <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> that is to be decoded.


### -param cbEncodedBlob [in]

The size, in bytes, of the encoded BLOB.


### -param dwPrevInnerContentType [in]

Only applicable when processing nested cryptographic messages. When processing an outer cryptographic message, it must be set to zero. When decoding a nested cryptographic message, it is set to the value returned at <i>pdwInnerContentType</i> by a previous calling of 
<b>CryptDecodeMessage</b> for the outer message. It can be any of the CMSG types listed in <i>pdwMsgType</i>. For backward compatibility, set <i>dwPrevInnerContentType</i> to zero.


### -param pdwMsgType [out, optional]

A pointer to a <b>DWORD</b> that specifies the message type returned. This parameter can be one of the following message types:

<ul>
<li>CMSG_DATA</li>
<li>CMSG_SIGNED</li>
<li>CMSG_ENVELOPED</li>
<li>CMSG_SIGNED_AND_ENVELOPED</li>
<li>CMSG_HASHED</li>
</ul>

### -param pdwInnerContentType [out, optional]

A pointer to a <b>DWORD</b> that specifies the type of an inner message. The message type codes used for <i>pdwMsgType</i> are used here, also. 




If there is no cryptographic nesting, CMSG_DATA is returned.


### -param pbDecoded [out, optional]

A pointer to a buffer to receive the decoded message. 




This parameter can be <b>NULL</b> if the decoded message is not required or to set the size of the decoded message for memory allocation purposes. A decoded message will not be returned if this parameter is <b>NULL</b>. For more information, see 
<a href="https://msdn.microsoft.com/ef99edef-39b2-4d78-9c01-13720215d47f">Retrieving Data of Unknown Length</a>.


### -param pcbDecoded [in, out, optional]

A pointer to a variable that specifies the size, in bytes, of the buffer pointed to by the <i>pbDecoded</i> parameter. When the function returns, this variable contains the size of the decoded message. 




<div class="alert"><b>Note</b>  When processing the data returned in the buffer, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data will fit in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

### -param ppXchgCert [out, optional]

A pointer to a 
pointer to a <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure with a certificate that corresponds to the private <a href="https://msdn.microsoft.com/f1caccd2-3453-448e-b194-bf899eff8091">exchange key</a> needed to decode the message. This parameter is only set for message types CMSG_ENVELOPED and CMSG_SIGNED_AND_ENVELOPED.


### -param ppSignerCert [out, optional]

A pointer to a 
pointer to a <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure of the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate context</a> of the signer. This parameter is only set for message types CMSG_SIGNED and CMSG_SIGNED_AND_ENVELOPED.


## -returns



If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The <a href="https://msdn.microsoft.com/e540b816-64e1-4c78-9020-2b221e813acc">CryptDecryptMessage</a>, 
<a href="https://msdn.microsoft.com/03411e7a-b097-4059-a198-3d412ae40e38">CryptVerifyMessageSignature</a>, or 
<a href="https://msdn.microsoft.com/3b5185b9-e24b-4302-a60c-74ccbd19077c">CryptVerifyMessageHash</a> functions can be propagated to this function.

The following error code is most commonly returned by the 
		       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

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
If the buffer specified by the <i>pbDecoded</i> parameter is not large enough to hold the returned data, the function sets the ERROR_MORE_DATA code and stores the required buffer size, in bytes, in the variable pointed to by <i>pcbDecoded</i>.

</td>
</tr>
</table>
 




## -remarks



The <i>dwMsgTypeFlags</i> parameter specifies the set of allowable messages. For example, to decode either SIGNED or ENVELOPED messages, set <i>dwMsgTypeFlags</i> to CMSG_SIGNED_FLAG | CMSG_ENVELOPED_FLAG. Either or both of the <i>pDecryptPara</i> or <i>pVerifyPara</i> parameters must be specified.

For a successfully decoded or verified message, the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate context</a> pointers pointed to by <i>ppXchgCert</i> and <i>ppSignerCert</i> are updated. They must be freed by calling 
<a href="https://msdn.microsoft.com/7d2f3237-3f8b-4234-b6db-3057384cd89b">CertFreeCertificateContext</a>. If the function fails, they are set to <b>NULL</b>.

The <i>ppXchgCert</i> or <i>ppSignerCert</i> parameters can be set to <b>NULL</b> before the function is called, which indicates that the caller is not interested in getting the exchange certificate or the signer <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate context</a>.




## -see-also




<a href="https://msdn.microsoft.com/e540b816-64e1-4c78-9020-2b221e813acc">CryptDecryptMessage</a>



<a href="https://msdn.microsoft.com/3b5185b9-e24b-4302-a60c-74ccbd19077c">CryptVerifyMessageHash</a>



<a href="https://msdn.microsoft.com/03411e7a-b097-4059-a198-3d412ae40e38">CryptVerifyMessageSignature</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Simplified Message Functions</a>
 

 

