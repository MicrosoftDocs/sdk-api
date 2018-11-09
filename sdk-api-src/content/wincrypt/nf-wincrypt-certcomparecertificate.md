---
UID: NF:wincrypt.CertCompareCertificate
title: CertCompareCertificate function
author: windows-sdk-content
description: Determines whether two certificates are identical by comparing the issuer name and serial number of the certificates.
old-location: security\certcomparecertificate.htm
tech.root: seccrypto
ms.assetid: b485fa81-b927-4f0c-bde1-075f36c76d9a
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: CertCompareCertificate, CertCompareCertificate function [Security], _crypto2_certcomparecertificate, security.certcomparecertificate, wincrypt/CertCompareCertificate
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
 - CertCompareCertificate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertCompareCertificate function


## -description


The <b>CertCompareCertificate</b> function determines whether two certificates are identical by comparing the issuer name and serial number of the certificates.
<div class="alert"><b>Caution</b>  The <b>CertCompareCertificate</b> function must not be used for security assertions because it does not compare <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOBs</a>.</div><div> </div>

## -parameters




### -param dwCertEncodingType [in]

Specifies the encoding type used. It is always acceptable to specify both the certificate and <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>



### -param pCertId1 [in]

A pointer to the 
<a href="https://msdn.microsoft.com/8d0a3053-52d4-437a-bf55-6724b5825cdc">CERT_INFO</a> for the first certificate in the comparison.


### -param pCertId2 [in]

A pointer to the <a href="https://msdn.microsoft.com/8d0a3053-52d4-437a-bf55-6724b5825cdc">CERT_INFO</a> for the second certificate in the comparison.


## -returns



If the certificates are identical and the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>).




## -see-also




<a href="https://msdn.microsoft.com/8d0a3053-52d4-437a-bf55-6724b5825cdc">CERT_INFO</a>



<a href="https://msdn.microsoft.com/6249429d-0cb2-4209-9580-87185d44b967">CertCompareCertificateName</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Data Management Functions</a>
 

 

