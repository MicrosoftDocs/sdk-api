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
					



