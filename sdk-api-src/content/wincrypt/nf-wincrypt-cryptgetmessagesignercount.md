---
UID: NF:wincrypt.CryptGetMessageSignerCount
title: CryptGetMessageSignerCount function
author: windows-sdk-content
description: The CryptGetMessageSignerCount function returns the number of signers of a signed message.
old-location: security\cryptgetmessagesignercount.htm
tech.root: seccrypto
ms.assetid: d18bda8b-b333-4b1e-8ed5-f8eff04b3168
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: CryptGetMessageSignerCount, CryptGetMessageSignerCount function [Security], _crypto2_cryptgetmessagesignercount, security.cryptgetmessagesignercount, wincrypt/CryptGetMessageSignerCount
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
 - CryptGetMessageSignerCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptGetMessageSignerCount function


## -description


The <b>CryptGetMessageSignerCount</b> function returns the number of signers of a signed message.


## -parameters




### -param dwMsgEncodingType [in]

Specifies the encoding type used. It is always acceptable to specify both the certificate and <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param pbSignedBlob [in]

A pointer to a buffer containing the signed message.


### -param cbSignedBlob [in]

The size, in bytes, of the signed message.


## -returns



Returns the number of signers of a signed message, zero when there are no signers, and minus one (–1) for an error.

For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. The following  error code is most commonly returned.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">message encoding type</a>. Currently only PKCS_7_ASN_ENCODING is supported.

</td>
</tr>
</table>
 

If the function fails, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> may return an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="https://msdn.microsoft.com/cb1f34dd-dab4-4ffb-a73b-79a214290509">ASN.1 Encoding/Decoding Return Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/03411e7a-b097-4059-a198-3d412ae40e38">CryptVerifyMessageSignature</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Simplified Message Functions</a>
 

 

