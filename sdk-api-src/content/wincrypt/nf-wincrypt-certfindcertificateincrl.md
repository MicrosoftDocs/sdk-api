---
UID: NF:wincrypt.CertFindCertificateInCRL
title: CertFindCertificateInCRL function
author: windows-sdk-content
description: The CertFindCertificateInCRL function searches the certificate revocation list (CRL) for the specified certificate.
old-location: security\certfindcertificateincrl.htm
tech.root: seccrypto
ms.assetid: c05a99e6-da38-431e-8d02-04056047a211
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CertFindCertificateInCRL, CertFindCertificateInCRL function [Security], _crypto2_certfindcertificateincrl, security.certfindcertificateincrl, wincrypt/CertFindCertificateInCRL
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
 - CertFindCertificateInCRL
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertFindCertificateInCRL function


## -description


The <b>CertFindCertificateInCRL</b> function searches the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL) for the specified certificate.
		


## -parameters




### -param pCert [in]

A pointer to a 
<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> of the certificate to be searched for in the CRL.


### -param pCrlContext [in]

A pointer to the 
<a href="https://msdn.microsoft.com/cf7cabcd-b469-492a-b855-8870465ea1cc">CRL_CONTEXT</a> to be searched.


### -param dwFlags [in]

Reserved for future use. Must be set to zero.


### -param pvReserved [in, optional]

Reserved for future use. Must be set to zero.


### -param ppCrlEntry [out]

If the certificate is found in the CRL, this pointer is updated with a pointer to the entry. Otherwise, it is set to <b>NULL</b>. The returned entry is not allocated and must not be freed.


## -returns



<b>TRUE</b> if the list was searched; otherwise <b>FALSE</b>.
					



