---
UID: NF:certenroll.IX509SCEPEnrollment.Initialize
title: IX509SCEPEnrollment::Initialize
author: windows-sdk-content
description: Initialize the instance in preparation for a new request.
old-location: security\ix509scepenrollment_initialize.htm
old-project: seccertenroll
ms.assetid: dcb887ab-c8b7-42e7-8b49-93755d24ba70
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IX509SCEPEnrollment interface [Security],Initialize method, IX509SCEPEnrollment.Initialize, IX509SCEPEnrollment::Initialize, Initialize, Initialize method [Security], Initialize method [Security],IX509SCEPEnrollment interface, certenroll/IX509SCEPEnrollment::Initialize, security.ix509scepenrollment_initialize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certenroll.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.dll
api_name:
 - IX509SCEPEnrollment.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: Certenroll.dll
req.irql: 
---

# IX509SCEPEnrollment::Initialize


## -description


Initialize the instance in preparation for a new request.


## -parameters




### -param pRequest [in]

An instance of a request that has already been initialized.


### -param strThumbprint [in]

The CA certificate thumbprint.


### -param ThumprintEncoding [in]

The encoding of the CA certificate thumbprint.


### -param strServerCertificates [in]

A PKCS7 request with CA and SCEP RA certificates.


### -param Encoding [in]

The encoding type of the request.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method expects an SCEP server signature EA certificate and an SCEP server encryption EA certificate, both signed by the CA certificate.

This method fails if any of the expected certificates is missing, or if the thumbprint doesn't match the CA certificate.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn424973(v=VS.85).aspx">IX509SCEPEnrollment</a>
 

 

