---
UID: NF:wincrypt.CryptMsgCountersignEncoded
title: CryptMsgCountersignEncoded function
author: windows-driver-content
description: Countersigns an existing PKCS #7 message signature.
old-location: security\cryptmsgcountersignencoded.htm
old-project: SecCrypto
ms.assetid: d9fd734b-e14d-4392-ac88-5565aefbedb4
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: CryptMsgCountersignEncoded, CryptMsgCountersignEncoded function [Security], _crypto2_cryptmsgcountersignencoded, security.cryptmsgcountersignencoded, wincrypt/CryptMsgCountersignEncoded
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Crypt32.dll
api_name:
-	CryptMsgCountersignEncoded
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CryptMsgCountersignEncoded function


## -description



			The <b>CryptMsgCountersignEncoded</b> function countersigns an existing PKCS #7 message signature. The <i>pbCountersignature</i> <b>BYTE</b> buffer it creates is a PKCS #7 encoded SignerInfo that can be used as an unauthenticated <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">Countersignature</a> attribute of a PKCS #9 signed-data or signed-and-enveloped-data message.


## -parameters




### -param dwEncodingType [in]

Specifies the encoding type used. Currently, only X509_ASN_ENCODING and PKCS_7_ASN_ENCODING are being used; however, additional encoding types may be added in the future. For either current encoding type, use: 


X509_ASN_ENCODING | PKCS_7_ASN_ENCODING.


### -param pbSignerInfo [in]

A pointer to the encoded SignerInfo that is to be countersigned.


### -param cbSignerInfo [in]

Count, in bytes, of the encoded SignerInfo data.


### -param cCountersigners [in]

Number of countersigners in the <i>rgCountersigners</i> array.


### -param rgCountersigners [in]

Array of countersigners' 
<a href="https://msdn.microsoft.com/f599226d-ddd7-455f-b650-74b91674d8f9">CMSG_SIGNER_ENCODE_INFO</a> structures.


### -param pbCountersignature [out]

A pointer to a buffer to receive an encoded PKCS #9 <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">countersignature</a> attribute.

On input, this parameter can be <b>NULL</b> to set the size of this information for memory allocation purposes. For more information, see 
<a href="https://msdn.microsoft.com/ef99edef-39b2-4d78-9c01-13720215d47f">Retrieving Data of Unknown Length</a>.


### -param pcbCountersignature [in, out]

A pointer to a variable that specifies the size, in bytes, of the buffer pointed to by the <i>pbCountersignature</i> parameter. When the function returns, the variable pointed to by the <i>pcbCountersignature</i> parameter contains the number of bytes stored in the buffer.


## -returns




						If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The following table lists the error codes most commonly returned by the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
 

Propagated errors might be returned from one of the following functions:

<ul>
<li>
<a href="https://msdn.microsoft.com/05e3db57-8d83-48e2-8590-68039ea27253">CryptCreateHash</a>
</li>
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
<a href="https://msdn.microsoft.com/b0d2610b-05ba-4fb6-8f38-10f970a52091">CryptMsgOpenToEncode</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d27d75f0-1646-4926-b375-59e52b00326c">CryptMsgUpdate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a990d44d-2993-429f-b817-2a834105ecef">CryptMsgControl</a>
</li>
</ul>
If the function fails, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> may return an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="https://msdn.microsoft.com/cb1f34dd-dab4-4ffb-a73b-79a214290509">ASN.1 Encoding/Decoding Return Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/ebf76664-bca6-462d-b519-2b60f435d8ef">CryptMsgCountersign</a>



<a href="https://msdn.microsoft.com/b0332360-a737-4b48-b592-0c55d493a02d">CryptMsgVerifyCountersignatureEncoded</a>



<a href="cryptography_functions.htm">Low-level Message Functions</a>



<a href="cryptography_functions.htm">Simplified Message Functions</a>
 

 

