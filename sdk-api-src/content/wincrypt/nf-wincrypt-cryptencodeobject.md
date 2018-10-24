---
UID: NF:wincrypt.CryptEncodeObject
title: CryptEncodeObject function
author: windows-sdk-content
description: The CryptEncodeObject function encodes a structure of the type indicated by the value of the lpszStructType parameter. The use of CryptEncodeObjectEx is recommended as an API that performs the same function with significant performance improvements.
old-location: security\cryptencodeobject.htm
tech.root: SecCrypto
ms.assetid: 9576a2a7-4379-4c1b-8ad5-284720cf7ccc
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: CryptEncodeObject, CryptEncodeObject function [Security], _crypto2_cryptencodeobject, security.cryptencodeobject, wincrypt/CryptEncodeObject
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
 - CryptEncodeObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptEncodeObject function


## -description


The <b>CryptEncodeObject</b> function encodes a structure of the type indicated by the value of the <i>lpszStructType</i> parameter. The use of 
<a href="https://msdn.microsoft.com/45134db8-059b-43d3-90c2-9b6cc970fca0">CryptEncodeObjectEx</a> is recommended as an API that performs the same function with significant performance improvements.


## -parameters




### -param dwCertEncodingType [in]

Type of encoding used. It is always acceptable to specify both the certificate and <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>
<div class="alert"><b>Note</b>  Either a certificate or <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">message encoding type</a> is required. X509_ASN_ENCODING is the default. If that type is indicated, it is used. Otherwise, if the PKCS7_ASN_ENCODING type is indicated, it is used.</div>
<div> </div>

### -param lpszStructType [in]

A pointer to an OID defining the structure type. If the high-order word of the <i>lpszStructType</i> parameter is zero, the low-order word specifies the integer identifier for the type of the specified structure. Otherwise, this parameter is a long pointer to a null-terminated string.

For more information about object identifier strings, their predefined constants and corresponding structures, see 
<a href="https://msdn.microsoft.com/f969f2a5-fcbb-4711-8523-ba22952ae952">Constants for CryptEncodeObject and CryptDecodeObject</a>.


### -param pvStructInfo [in]

A pointer to the structure to be encoded. The structure must be of a type specified by <i>lpszStructType</i>.


### -param pbEncoded [out]

A pointer to a buffer to receive the encoded structure. When the buffer that is specified is not large enough to receive the decoded structure, the function sets the ERROR_MORE_DATA code and stores the required buffer size, in bytes, in the variable pointed to by <i>pcbEncoded</i>.

This parameter can be <b>NULL</b> to retrieve the size of this information for memory allocation purposes. For more information, see 
<a href="https://msdn.microsoft.com/ef99edef-39b2-4d78-9c01-13720215d47f">Retrieving Data of Unknown Length</a>.


### -param pcbEncoded [in, out]

A pointer to a <b>DWORD</b> variable that contains the size, in bytes, of the buffer pointed to by the <i>pbEncoded</i> parameter. When the function returns, the <b>DWORD</b> value contains the number of allocated encoded bytes stored in the buffer.

<div class="alert"><b>Note</b>  When processing the data returned in the buffer, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data fits in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

## -returns



If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Some possible error codes are listed in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_BAD_ENCODE</b></dt>
</dl>
</td>
<td width="60%">
An error was encountered while encoding.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
An encoding function could not be found for the specified <i>dwCertEncodingType</i> and <i>lpszStructType</i>.
							

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
If the buffer specified by the <i>pbEncoded</i> parameter is not large enough to hold the returned data, the function sets the ERROR_MORE_DATA code and stores the required buffer size, in bytes, in the variable pointed to by <i>pcbEncoded</i>.

</td>
</tr>
</table>
 

If the function fails, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> may return an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="https://msdn.microsoft.com/cb1f34dd-dab4-4ffb-a73b-79a214290509">ASN.1 Encoding/Decoding Return Values</a>.




## -remarks



When encoding a cryptographic object using the preferred <a href="https://msdn.microsoft.com/45134db8-059b-43d3-90c2-9b6cc970fca0">CryptEncodeObjectEx</a> function, the terminating <b>NULL</b> character is included. When decoding, using the preferred <a href="https://msdn.microsoft.com/bf1935f0-1ab0-4068-9ed5-8fbb2c286b8a">CryptDecodeObjectEx</a> function, the terminating <b>NULL</b> character is not retained.


#### Examples

For an example that uses this function, see 
<a href="https://msdn.microsoft.com/bd3d0259-f0e8-460e-9f18-95d2492da3d8">Example C Program: Making a Certificate Request</a> and 
<a href="https://msdn.microsoft.com/78108cd5-531e-4d0c-96cf-6f6264b7716c">Example C Program: ASN.1 Encoding and Decoding</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/7d5ed4f4-9d76-4a16-9059-27b0edd83459">CryptDecodeObject</a>



<a href="https://msdn.microsoft.com/45134db8-059b-43d3-90c2-9b6cc970fca0">CryptEncodeObjectEx</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Object Encoding and Decoding Functions</a>
 

 

