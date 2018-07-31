---
UID: NF:wincrypt.CryptMsgOpenToDecode
title: CryptMsgOpenToDecode function
author: windows-sdk-content
description: Opens a cryptographic message for decoding and returns a handle of the opened message.
old-location: security\cryptmsgopentodecode.htm
old-project: SecCrypto
ms.assetid: b3df6312-c866-4faa-8b89-bda67c697631
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: CMSG_CRYPT_RELEASE_CONTEXT_FLAG, CMSG_DATA, CMSG_DETACHED_FLAG, CMSG_ENVELOPED, CMSG_HASHED, CMSG_SIGNED, CMSG_SIGNED_AND_ENVELOPED, CryptMsgOpenToDecode, CryptMsgOpenToDecode function [Security], _crypto2_cryptmsgopentodecode, security.cryptmsgopentodecode, wincrypt/CryptMsgOpenToDecode
ms.prod: windows
ms.technology: windows-sdk
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
 - CryptMsgOpenToDecode
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CryptMsgOpenToDecode function


## -description


The <b>CryptMsgOpenToDecode</b> function opens a cryptographic message for decoding and returns a handle of the opened message. The message remains open until 
the <a href="https://msdn.microsoft.com/2478dd60-233a-4ef3-86e9-62d2a59ab28a">CryptMsgClose</a> function is called.

Important changes that affect the handling of enveloped messages have been made to CryptoAPI to support <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">Secure/Multipurpose Internet Mail Extensions</a> (S/MIME) email interoperability. For details, see the Remarks section of 
<a href="https://msdn.microsoft.com/b0d2610b-05ba-4fb6-8f38-10f970a52091">CryptMsgOpenToEncode</a>.


## -parameters




### -param dwMsgEncodingType [in]

Specifies the encoding type used. It is always acceptable to specify both the certificate and <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING


Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>



### -param dwFlags [in]

This parameter can be one of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CMSG_DETACHED_FLAG"></a><a id="cmsg_detached_flag"></a><dl>
<dt><b>CMSG_DETACHED_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the message to be decoded is detached. If this flag is not set, the message is not detached.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CRYPT_RELEASE_CONTEXT_FLAG"></a><a id="cmsg_crypt_release_context_flag"></a><dl>
<dt><b>CMSG_CRYPT_RELEASE_CONTEXT_FLAG</b></dt>
</dl>
</td>
<td width="60%">
If set, the <i>hCryptProv</i> passed to this function is released on the final <a href="https://msdn.microsoft.com/d27d75f0-1646-4926-b375-59e52b00326c">CryptMsgUpdate</a>. The handle is not released if the function fails.

</td>
</tr>
</table>
 


### -param dwMsgType [in]

Specifies the type of message to decode. In most cases, the message type is determined from the message header and zero is passed for this parameter. In some cases, notably with Internet Explorer 3.0, messages do not have headers and the type of message to be decoded must be supplied in this function call. If the header is missing and zero is passed for this parameter, the function fails.


This parameter can be one of the following predefined message types.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CMSG_DATA"></a><a id="cmsg_data"></a><dl>
<dt><b>CMSG_DATA</b></dt>
</dl>
</td>
<td width="60%">
The message is encoded data.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_ENVELOPED"></a><a id="cmsg_enveloped"></a><dl>
<dt><b>CMSG_ENVELOPED</b></dt>
</dl>
</td>
<td width="60%">
The message is an enveloped message.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_HASHED"></a><a id="cmsg_hashed"></a><dl>
<dt><b>CMSG_HASHED</b></dt>
</dl>
</td>
<td width="60%">
The message is a hashed message.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_SIGNED"></a><a id="cmsg_signed"></a><dl>
<dt><b>CMSG_SIGNED</b></dt>
</dl>
</td>
<td width="60%">
The message is a signed message.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_SIGNED_AND_ENVELOPED"></a><a id="cmsg_signed_and_enveloped"></a><dl>
<dt><b>CMSG_SIGNED_AND_ENVELOPED</b></dt>
</dl>
</td>
<td width="60%">
The message is a signed and enveloped message.

</td>
</tr>
</table>
 


### -param hCryptProv [in]

This parameter is not used and should be set to <b>NULL</b>.

<b>Windows Server 2003 and Windows XP:  </b>Specifies a handle for the cryptographic provider to use for <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hashing</a> the message. For signed messages, <i>hCryptProv</i> is used for signature verification.This parameter's data type is <b>HCRYPTPROV</b>.

Unless there is a strong reason for passing in a specific cryptographic provider in <i>hCryptProv</i>, set this parameter to <b>NULL</b>. Passing in <b>NULL</b> causes the default RSA or DSS provider to be acquired before performing hash, signature verification, or recipient encryption operations.




### -param pRecipientInfo [in]

This parameter is reserved for future use and must be <b>NULL</b>.


### -param pStreamInfo [in, optional]

When streaming is not being used, this parameter must be set to <b>NULL</b>.


<div class="alert"><b>Note</b>  Streaming is not used with CMSG_HASHED messages. When dealing with hashed data, this parameter must be set to <b>NULL</b>.</div>
<div> </div>


When streaming is being used, the <i>pStreamInfo</i> parameter is a pointer to a 
<a href="https://msdn.microsoft.com/a4e7f6e8-351f-4981-b223-50b65f503394">CMSG_STREAM_INFO</a> structure that contains a pointer to a callback to be called when 
<a href="https://msdn.microsoft.com/d27d75f0-1646-4926-b375-59e52b00326c">CryptMsgUpdate</a> is executed or when 
<a href="https://msdn.microsoft.com/a990d44d-2993-429f-b817-2a834105ecef">CryptMsgControl</a> is executed when decoding a streamed enveloped message.

For a signed message, the callback is passed a block of the decoded bytes from the <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">inner content</a> of the message.

For an enveloped message, after each call to <a href="https://msdn.microsoft.com/d27d75f0-1646-4926-b375-59e52b00326c">CryptMsgUpdate</a>, you must check to determine whether the CMSG_ENVELOPE_ALGORITHM_PARAM property is available by calling 
the <a href="https://msdn.microsoft.com/5a05eb09-208f-4e94-abfa-c2f14c0a3164">CryptMsgGetParam</a> function. <b>CryptMsgGetParam</b> will fail and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> will return CRYPT_E_STREAM_MSG_NOT_READY until 
<b>CryptMsgUpdate</b> has processed enough of the message to make the CMSG_ENVELOPE_ALGORITHM_PARAM property available. When the CMSG_ENVELOPE_ALGORITHM_PARAM property is available, you can iterate through the recipients, retrieving a 
<a href="https://msdn.microsoft.com/8d0a3053-52d4-437a-bf55-6724b5825cdc">CERT_INFO</a> structure for each recipient by using the <b>CryptMsgGetParam</b> function to retrieve the CMSG_RECIPIENT_INFO_PARAM property. To prevent a denial of service attack from an enveloped message that has an artificially large header block, you must keep track of the amount of memory that has been passed to the <b>CryptMsgUpdate</b> function during this process.  If the amount of data exceeds an application defined limit before the CMSG_ENVELOPE_ALGORITHM_PARAM property is available, you must stop processing the message and call the <a href="https://msdn.microsoft.com/2478dd60-233a-4ef3-86e9-62d2a59ab28a">CryptMsgClose</a> function to cause the operating system to release any memory that has been allocated for the message. A suggested limit is the maximum allowable size of a message. For example, if the maximum message size is 10 MB, the limit for this test should be 10 MB.

The <a href="https://msdn.microsoft.com/8d0a3053-52d4-437a-bf55-6724b5825cdc">CERT_INFO</a> structure is used to find a matching certificate in a previously opened <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a> by using 
the <a href="https://msdn.microsoft.com/61d73501-91b1-4498-b1a3-17392360c700">CertGetSubjectCertificateFromStore</a> function. When the correct certificate is found, 
the <a href="https://msdn.microsoft.com/f766db64-3121-4f70-ac83-ce25ee634efa">CertGetCertificateContextProperty</a> function with a CERT_KEY_PROV_INFO_PROP_ID parameter is called to retrieve a 
<a href="https://msdn.microsoft.com/6aea2f47-9d4a-4069-ac6d-f28907df00be">CRYPT_KEY_PROV_INFO</a> structure. The structure contains the information necessary to acquire the recipient's private key by calling 
<a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a>, using the <b>pwszContainerName</b>, <b>pwszProvName</b>, <b>dwProvType</b>, and <b>dwFlags</b> members of the <b>CRYPT_KEY_PROV_INFO</b> structure. The <b>hCryptProv</b> acquired and the <b>dwKeySpec</b> member of the <b>CRYPT_KEY_PROV_INFO</b> structure are passed to 
the <a href="https://msdn.microsoft.com/a990d44d-2993-429f-b817-2a834105ecef">CryptMsgControl</a> structure as a member of the 
<a href="https://msdn.microsoft.com/eb9b1daa-b04f-419a-88e3-7c772f9e62eb">CMSG_CTRL_DECRYPT_PARA</a> structure to permit the start of the decryption of the <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">inner content</a>. The streaming code will then perform the decryption as the data is input. The resulting blocks of <a href="https://msdn.microsoft.com/library/windows/hardware/dn965962">plaintext</a> are passed to the callback function specified by the <b>pfnStreamOutput</b> member of the <a href="https://msdn.microsoft.com/a4e7f6e8-351f-4981-b223-50b65f503394">CMSG_STREAM_INFO</a> structure to handle the output of the decrypted message.


<div class="alert"><b>Note</b>  Streamed decoding of an enveloped message queues the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">ciphertext</a> in memory until <a href="https://msdn.microsoft.com/a990d44d-2993-429f-b817-2a834105ecef">CryptMsgControl</a> is called to start the decryption. The application must initiate decrypting in a timely manner so that the data can be saved to disk or routed elsewhere before the accumulated <i>ciphertext</i> becomes too large and the system runs out of memory.</div>
<div> </div>


In the case of a signed message enclosed in an enveloped message, the <a href="https://msdn.microsoft.com/library/windows/hardware/dn965962">plaintext</a> output from the streaming decode of the enveloped message can be fed into another streaming decode to process the signed message.


## -returns



If the function succeeds, the function returns the handle of the opened message.

If the function fails, it returns <b>NULL</b>. For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The following table lists the error codes most commonly returned by the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

<table>
<tr>
<th>Value</th>
<th>Description</th>
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
A memory allocation failure occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/2478dd60-233a-4ef3-86e9-62d2a59ab28a">CryptMsgClose</a>



<a href="https://msdn.microsoft.com/5a05eb09-208f-4e94-abfa-c2f14c0a3164">CryptMsgGetParam</a>



<a href="https://msdn.microsoft.com/b0d2610b-05ba-4fb6-8f38-10f970a52091">CryptMsgOpenToEncode</a>



<a href="https://msdn.microsoft.com/d27d75f0-1646-4926-b375-59e52b00326c">CryptMsgUpdate</a>



<a href="cryptography_functions.htm">Low-level Message Functions</a>



<a href="cryptography_functions.htm">Simplified Message Functions</a>
 

 

