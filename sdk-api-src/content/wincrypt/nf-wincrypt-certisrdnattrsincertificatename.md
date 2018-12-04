---
UID: NF:wincrypt.CertIsRDNAttrsInCertificateName
title: CertIsRDNAttrsInCertificateName function
author: windows-sdk-content
description: The CertIsRDNAttrsInCertificateName function compares the attributes in the certificate name with the specified CERT_RDN to determine whether all attributes are included there.
old-location: security\certisrdnattrsincertificatename.htm
tech.root: seccrypto
ms.assetid: e45b80a3-9269-4f21-8407-1c8303cb5f32
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: CertIsRDNAttrsInCertificateName, CertIsRDNAttrsInCertificateName function [Security], _crypto2_certisrdnattrsincertificatename, security.certisrdnattrsincertificatename, wincrypt/CertIsRDNAttrsInCertificateName
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
 - CertIsRDNAttrsInCertificateName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertIsRDNAttrsInCertificateName function


## -description


The <b>CertIsRDNAttrsInCertificateName</b> function compares the attributes in the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate name</a> with the specified 
<a href="https://msdn.microsoft.com/e84254b9-e9a7-4689-a12f-2772282c5433">CERT_RDN</a> to determine whether all attributes are included there. The comparison iterates through the <b>CERT_RDN</b> and looks for an attribute match in any of the <b>CERT_RDN</b>s of the certificate name.


## -parameters




### -param dwCertEncodingType [in]

Specifies the encoding type used. It is always acceptable to specify both the certificate and <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param dwFlags [in]

CERT_UNICODE_IS_RDN_ATTRS_FLAG must be set if the <i>pRDN</i> was initialized with Unicode strings as in 
<a href="https://msdn.microsoft.com/9576a2a7-4379-4c1b-8ad5-284720cf7ccc">CryptEncodeObject</a> with <i>lpszStructType</i> set to X509_UNICODE_NAME.

CERT_CASE_INSENSITIVE_IS_RDN_ATTRS_FLAG is set to do a case insensitive match. Otherwise, an exact, case sensitive match is done.


### -param pCertName [in]

A pointer to a 
<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a> that contains the encoded subject or issuer name.


### -param pRDN [in]

Array of 
<a href="https://msdn.microsoft.com/e84254b9-e9a7-4689-a12f-2772282c5433">CERT_RDN</a> structures that contain the attributes to be found in the name. The 
<a href="https://msdn.microsoft.com/4729e824-761c-4115-8b7b-76ffdab8ea62">CERT_RDN_ATTR</a> member of the <b>CERT_RDN</b> structure behaves according to the following rules.

<ul>
<li>If <b>pszObjId</b> is <b>NULL</b>, the attribute <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) is ignored.</li>
<li>If <b>dwValueType</b> is CERT_RDN_ANY_TYPE, the value type is ignored.</li>
<li>If the <b>pbData</b> member of <b>Value</b> is  <b>NULL</b>, any value can be a match.</li>
</ul>

## -returns



If the function succeeds and all of the RDN values in the specified <a href="https://msdn.microsoft.com/e84254b9-e9a7-4689-a12f-2772282c5433">CERT_RDN</a> are in the certificate name, the return value is nonzero (<b>TRUE</b>).

If the function fails, or if there are  RDN values in the specified <a href="https://msdn.microsoft.com/e84254b9-e9a7-4689-a12f-2772282c5433">CERT_RDN</a> that are not in the certificate name, the return value is zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The following table lists some possible error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_NO_MATCH</b></dt>
</dl>
</td>
<td width="60%">
Not all the attributes were found and matched.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Invalid certificate encoding type. Currently only X509_ASN_ENCODING is supported.

</td>
</tr>
</table>
 

If the function fails, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> may return an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="https://msdn.microsoft.com/cb1f34dd-dab4-4ffb-a73b-79a214290509">ASN.1 Encoding/Decoding Return Values</a>.




## -remarks



Currently, only an exact, case-sensitive match is supported.




## -see-also




<a href="https://msdn.microsoft.com/20b3fcfb-55df-46ff-80a5-70f31a3d03b2">CertFindCertificateInStore</a>



<a href="cryptography_functions.htm">Data Management Functions</a>
 

 

