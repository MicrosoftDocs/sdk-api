---
UID: NF:wincrypt.CryptMsgCalculateEncodedLength
title: CryptMsgCalculateEncodedLength function
author: windows-sdk-content
description: Calculates the maximum number of bytes needed for an encoded cryptographic message given the message type, encoding parameters, and total length of the data to be encoded.
old-location: security\cryptmsgcalculateencodedlength.htm
tech.root: seccrypto
ms.assetid: 1c12003a-c2f3-4069-8bd6-b8f2875b0c98
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: CMSG_BARE_CONTENT_FLAG, CMSG_CMS_ENCAPSULATED_CONTENT_FLAG, CMSG_CONTENTS_OCTETS_FLAG, CMSG_DATA, CMSG_DETACHED_FLAG, CMSG_ENCRYPTED, CMSG_ENVELOPED, CMSG_HASHED, CMSG_SIGNED, CMSG_SIGNED_AND_ENVELOPED, CryptMsgCalculateEncodedLength, CryptMsgCalculateEncodedLength function [Security], _crypto2_cryptmsgcalculateencodedlength, security.cryptmsgcalculateencodedlength, wincrypt/CryptMsgCalculateEncodedLength
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
 - CryptMsgCalculateEncodedLength
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CryptMsgCalculateEncodedLength
: 
---

# CryptMsgCalculateEncodedLength function


## -description


The <b>CryptMsgCalculateEncodedLength</b> function calculates the maximum number of bytes needed for an encoded cryptographic message given the message type, encoding parameters, and total length of the data to be encoded. Note that the result will always be greater than or equal to the actual number of bytes needed.


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

Currently defined flags are shown in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CMSG_BARE_CONTENT_FLAG"></a><a id="cmsg_bare_content_flag"></a><dl>
<dt><b>CMSG_BARE_CONTENT_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Indicates that streamed output will not have an outer ContentInfo wrapper (as defined by PKCS #7). This makes it suitable to be streamed into an enclosing message.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_DETACHED_FLAG"></a><a id="cmsg_detached_flag"></a><dl>
<dt><b>CMSG_DETACHED_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Indicates that there is detached data being supplied for the subsequent calls to 
<a href="https://msdn.microsoft.com/d27d75f0-1646-4926-b375-59e52b00326c">CryptMsgUpdate</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CONTENTS_OCTETS_FLAG"></a><a id="cmsg_contents_octets_flag"></a><dl>
<dt><b>CMSG_CONTENTS_OCTETS_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Used to calculate the size of a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">DER</a> encoding of a message to be nested inside an enveloped message. This is particularly useful when streaming is being performed.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_CMS_ENCAPSULATED_CONTENT_FLAG"></a><a id="cmsg_cms_encapsulated_content_flag"></a><dl>
<dt><b>CMSG_CMS_ENCAPSULATED_CONTENT_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Non-Data type <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">inner content</a> is encapsulated within an OCTET STRING. This flag is applicable for both Signed and Enveloped messages.

</td>
</tr>
</table>
 


### -param dwMsgType [in]

Currently defined message types are shown in the following table.

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
An octet (BYTE) string.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_SIGNED"></a><a id="cmsg_signed"></a><dl>
<dt><b>CMSG_SIGNED</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/93138744-8316-461b-908a-1eab47e83f63">CMSG_SIGNED_ENCODE_INFO</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_ENVELOPED"></a><a id="cmsg_enveloped"></a><dl>
<dt><b>CMSG_ENVELOPED</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/87712541-2806-4709-a7cf-c9ba966c96fd">CMSG_ENVELOPED_ENCODE_INFO</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_SIGNED_AND_ENVELOPED"></a><a id="cmsg_signed_and_enveloped"></a><dl>
<dt><b>CMSG_SIGNED_AND_ENVELOPED</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_HASHED"></a><a id="cmsg_hashed"></a><dl>
<dt><b>CMSG_HASHED</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/05dfeda0-a8a1-4203-a68a-af92903ab215">CMSG_HASHED_ENCODE_INFO</a>


</td>
</tr>
<tr>
<td width="40%"><a id="CMSG_ENCRYPTED"></a><a id="cmsg_encrypted"></a><dl>
<dt><b>CMSG_ENCRYPTED</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
</table>
 


### -param pvMsgEncodeInfo [in]

A pointer to the data to be encoded. The type of data pointed to depends on the value of <i>dwMsgType</i>. For details, see the <i>dwMsgType</i> table.


### -param pszInnerContentObjID [in, optional]

When calling <b>CryptMsgCalculateEncodedLength</b> with data provided to 
<a href="https://msdn.microsoft.com/d27d75f0-1646-4926-b375-59e52b00326c">CryptMsgUpdate</a> already encoded, the appropriate object identifier is passed in <i>pszInnerContentObjID</i>. If <i>pszInnerContentObjID</i> is <b>NULL</b>, the <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">inner content</a> type is assumed not to have been previously encoded, and is encoded as an octet string and given the type CMSG_DATA. 




When streaming is being used, <i>pszInnerContentObjID</i> must be either <b>NULL</b> or szOID_RSA_data.

The following algorithm object identifiers are commonly used:

<ul>
<li>szOID_RSA_data</li>
<li>szOID_RSA_signedData</li>
<li>szOID_RSA_envelopedData</li>
<li>szOID_RSA_signEnvData</li>
<li>szOID_RSA_digestedData</li>
<li>szOID_RSA_encryptedData</li>
<li>SPC_INDIRECT_DATA_OBJID</li>
</ul>
A user can define new <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">inner content</a> usage. The user must ensure that the sender and receiver of the message agree upon the semantics associated with the object identifier.


### -param cbData [in]

The size, in bytes, of the content.


## -returns



Returns the required length for an encoded cryptographic message. This length might not be the exact length but it will not be less than the required length. Zero is returned if the function fails.

To retrieve extended error information, use the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function. The following table lists the error codes most commonly returned.

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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b0d2610b-05ba-4fb6-8f38-10f970a52091">CryptMsgOpenToEncode</a>



<a href="cryptography_functions.htm">Low-level Message Functions</a>



<a href="cryptography_functions.htm">Simplified Message Functions</a>
 

 

