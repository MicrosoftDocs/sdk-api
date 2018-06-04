---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# CryptMsgEncodeAndSignCTL function


## -description



			The <b>CryptMsgEncodeAndSignCTL</b> function encodes a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">CTL</a> and creates a signed message containing the encoded CTL.

This function first encodes the CTL pointed to by <i>pCtlInfo</i> and then calls 
<a href="https://msdn.microsoft.com/85ae8ce3-d0a7-4fcb-beaa-ede09d30930e">CryptMsgSignCTL</a> to sign the encoded message.


## -parameters




### -param dwMsgEncodingType [in]

Specifies the encoding type used. It is always acceptable to specify both the certificate and <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param pCtlInfo [in]

A pointer to the 
<a href="https://msdn.microsoft.com/83b015b5-a650-4a81-a9f0-c3e8a9805c81">CTL_INFO</a> structure containing the CTL to be encoded and signed.


### -param pSignInfo [in]

A pointer to a 
<a href="https://msdn.microsoft.com/93138744-8316-461b-908a-1eab47e83f63">CMSG_SIGNED_ENCODE_INFO</a> structure that contains an array of a 
<a href="https://msdn.microsoft.com/f599226d-ddd7-455f-b650-74b91674d8f9">CMSG_SIGNER_ENCODE_INFO</a> structures.

The message can be encoded without signers if the <b>cbSize</b> member of the structure is set to the size of the structure and all of the other members are set to zero.


### -param dwFlags [in]

CMSG_ENCODE_SORTED_CTL_FLAG is set if the CTL entries are to be sorted before encoding. This flag is set if the 
<a href="https://msdn.microsoft.com/027e89e6-3de0-440d-be70-2281778f9a1e">CertFindSubjectInSortedCTL</a> or <a href="https://msdn.microsoft.com/b37cff03-5e9c-4e6c-b46e-d3f02dbf8783">CertEnumSubjectInSortedCTL</a> functions will be called.

CMSG_ENCODE_HASHED_SUBJECT_IDENTIFIER_FLAG is set if CMSG_ENCODE_SORTED_CTL_FLAG is set, and the identifier for the TrustedSubjects is a hash, such as MD5 or SHA1.

If CMS_PKCS7 is defined, <i>dwFlags</i> can be set to CMSG_CMS_ENCAPSULATED_CTL_FLAG to encode a CMS compatible V3 SignedData message.


### -param pbEncoded [out]

A pointer to a buffer that receives the encoded, signed message created.

This parameter can be <b>NULL</b> to set the size of this information for memory allocation purposes. For more information, see 
<a href="https://msdn.microsoft.com/ef99edef-39b2-4d78-9c01-13720215d47f">Retrieving Data of Unknown Length</a>.


### -param pcbEncoded [in, out]

A pointer to a <b>DWORD</b> that specifies the size, in bytes, of the <i>pbEncoded</i> buffer. When the function returns, the <b>DWORD</b> contains the number of bytes stored or to be stored in the buffer.


## -returns




						If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Errors can be propagated from calls to 
<a href="https://msdn.microsoft.com/b0d2610b-05ba-4fb6-8f38-10f970a52091">CryptMsgOpenToEncode</a> and 
<a href="https://msdn.microsoft.com/d27d75f0-1646-4926-b375-59e52b00326c">CryptMsgUpdate</a>.




## -see-also




<a href="https://msdn.microsoft.com/93138744-8316-461b-908a-1eab47e83f63">CMSG_SIGNED_ENCODE_INFO</a>



<a href="https://msdn.microsoft.com/83b015b5-a650-4a81-a9f0-c3e8a9805c81">CTL_INFO</a>



<a href="https://msdn.microsoft.com/b37cff03-5e9c-4e6c-b46e-d3f02dbf8783">CertEnumSubjectInSortedCTL</a>



<a href="https://msdn.microsoft.com/027e89e6-3de0-440d-be70-2281778f9a1e">CertFindSubjectInSortedCTL</a>



<a href="https://msdn.microsoft.com/b0d2610b-05ba-4fb6-8f38-10f970a52091">CryptMsgOpenToEncode</a>



<a href="https://msdn.microsoft.com/85ae8ce3-d0a7-4fcb-beaa-ede09d30930e">CryptMsgSignCTL</a>



<a href="cryptography_functions.htm">Verification Functions Using CTLs</a>
 

 

