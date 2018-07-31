---
UID: NF:wincrypt.CertCompareCertificateName
title: CertCompareCertificateName function
author: windows-sdk-content
description: The CertCompareCertificateName function compares two certificate CERT_NAME_BLOB structures to determine whether they are identical. The CERT_NAME_BLOB structures are used for the subject and the issuer of certificates.
old-location: security\certcomparecertificatename.htm
old-project: SecCrypto
ms.assetid: 6249429d-0cb2-4209-9580-87185d44b967
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: CertCompareCertificateName, CertCompareCertificateName function [Security], _crypto2_certcomparecertificatename, security.certcomparecertificatename, wincrypt/CertCompareCertificateName
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
 - CertCompareCertificateName
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CertCompareCertificateName function


## -description


The <b>CertCompareCertificateName</b> function compares two certificate 
<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CERT_NAME_BLOB</a> structures to determine whether they are identical. The <b>CERT_NAME_BLOB</b> structures are used for the subject and the issuer of certificates.


## -parameters




### -param dwCertEncodingType [in]

Specifies the encoding type used. It is always acceptable to specify both the certificate and <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>



### -param pCertName1 [in]

A pointer to a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CERT_NAME_BLOB</a> for the first name in the comparison. For more information, see 
<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a>.


### -param pCertName2 [in]

A pointer to a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CERT_NAME_BLOB</a> for the second name in the comparison.


## -returns



If the names are identical and the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>).




## -see-also




<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CERT_NAME_BLOB</a>



<a href="https://msdn.microsoft.com/b485fa81-b927-4f0c-bde1-075f36c76d9a">CertCompareCertificate</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Data Management Functions</a>
 

 

