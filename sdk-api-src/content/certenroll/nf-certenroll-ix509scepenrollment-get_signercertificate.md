---
UID: NF:certenroll.IX509SCEPEnrollment.get_SignerCertificate
title: IX509SCEPEnrollment::get_SignerCertificate
author: windows-sdk-content
description: Gets or sets the signer certificate for the request.
old-location: security\ix509scepenrollment_signercertificate.htm
tech.root: seccertenroll
ms.assetid: 7d01acc5-158d-4429-a2e8-d179571f9a1c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IX509SCEPEnrollment interface [Security],SignerCertificate property, IX509SCEPEnrollment.SignerCertificate, IX509SCEPEnrollment.get_SignerCertificate, IX509SCEPEnrollment::SignerCertificate, IX509SCEPEnrollment::get_SignerCertificate, IX509SCEPEnrollment::put_SignerCertificate, SignerCertificate property [Security], SignerCertificate property [Security],IX509SCEPEnrollment interface, certenroll/IX509SCEPEnrollment::SignerCertificate, certenroll/IX509SCEPEnrollment::get_SignerCertificate, certenroll/IX509SCEPEnrollment::put_SignerCertificate, get_SignerCertificate, security.ix509scepenrollment_signercertificate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certenroll.h
req.include-header: 
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
req.lib: 
req.dll: Certenroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.dll
api_name:
 - IX509SCEPEnrollment.SignerCertificate
 - IX509SCEPEnrollment.get_SignerCertificate
 - IX509SCEPEnrollment.put_SignerCertificate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509SCEPEnrollment::get_SignerCertificate


## -description


Gets or sets the signer certificate for the request.

This property is read/write.


## -parameters


## -remarks



To create a renewal request, you must set this property prior to calling the <a href="https://msdn.microsoft.com/en-us/library/Dn424976(v=VS.85).aspx">CreateRequestMessage</a> method. Otherwise, the <b>CreateRequestMessage</b> method will create a new request and generate a self-signed certificate using the same private key as the inner PKCSV10 reqeust.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn424973(v=VS.85).aspx">IX509SCEPEnrollment</a>
 

 

