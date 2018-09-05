---
UID: NF:certenroll.IX509SCEPEnrollment.CreateRetrieveCertificateMessage
title: IX509SCEPEnrollment::CreateRetrieveCertificateMessage
author: windows-sdk-content
description: Retrieve a previously issued certificate.
old-location: security\ix509scepenrollment_createretrievecertificatemessage.htm
old-project: SecCertEnroll
ms.assetid: 238a837f-4464-49ce-b87a-03abcfc0abea
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CreateRetrieveCertificateMessage, CreateRetrieveCertificateMessage method [Security], CreateRetrieveCertificateMessage method [Security],IX509SCEPEnrollment interface, IX509SCEPEnrollment interface [Security],CreateRetrieveCertificateMessage method, IX509SCEPEnrollment.CreateRetrieveCertificateMessage, IX509SCEPEnrollment::CreateRetrieveCertificateMessage, certenroll/IX509SCEPEnrollment::CreateRetrieveCertificateMessage, security.ix509scepenrollment_createretrievecertificatemessage
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
 - IX509SCEPEnrollment.CreateRetrieveCertificateMessage
product: Windows
targetos: Windows
req.lib: 
req.dll: Certenroll.dll
req.irql: 
---

# IX509SCEPEnrollment::CreateRetrieveCertificateMessage


## -description


Retrieve a previously issued certificate.


## -parameters




### -param Context [in]


### -param strIssuer [in]

ASN.1 encoded issuer name.


### -param IssuerEncoding [in]


### -param strSerialNumber [in]


### -param SerialNumberEncoding [in]


### -param Encoding [in]


### -param pValue [out, retval]


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You must call the <a href="https://msdn.microsoft.com/6b6f9e9d-5316-4928-861a-22497e1f5c00">InitializeForPending</a> method before calling this method.




## -see-also




<a href="https://msdn.microsoft.com/fcbac911-9e37-4994-bbb6-544b19a92749">IX509SCEPEnrollment</a>
 

 

