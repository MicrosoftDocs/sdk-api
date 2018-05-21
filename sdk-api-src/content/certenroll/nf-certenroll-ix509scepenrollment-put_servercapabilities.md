---
UID: NF:certenroll.IX509SCEPEnrollment.put_ServerCapabilities
title: IX509SCEPEnrollment::put_ServerCapabilities
author: windows-driver-content
description: Sets the preferred hash and encryption algorithms for the request.
old-location: security\ix509scepenrollment_servercapabilities.htm
old-project: SecCertEnroll
ms.assetid: fcfed23f-7798-4b56-afcd-65975a2d39bd
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: IX509SCEPEnrollment interface [Security],ServerCapabilities property, IX509SCEPEnrollment.ServerCapabilities, IX509SCEPEnrollment.put_ServerCapabilities, IX509SCEPEnrollment::ServerCapabilities, IX509SCEPEnrollment::put_ServerCapabilities, ServerCapabilities property [Security], ServerCapabilities property [Security],IX509SCEPEnrollment interface, certenroll/IX509SCEPEnrollment::ServerCapabilities, certenroll/IX509SCEPEnrollment::put_ServerCapabilities, put_ServerCapabilities, security.ix509scepenrollment_servercapabilities
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Certenroll.dll
api_name:
-	IX509SCEPEnrollment.ServerCapabilities
-	IX509SCEPEnrollment.put_ServerCapabilities
product: Windows
targetos: Windows
req.lib: 
req.dll: Certenroll.dll
req.irql: 
---

# IX509SCEPEnrollment::put_ServerCapabilities


## -description


Sets the preferred hash and encryption algorithms for the request.

This property is write-only.


## -parameters


## -remarks



If you do not set this property, then the default hash and encryption algorithms will be used.

This property must be set before calling the <a href="https://msdn.microsoft.com/b86d6dc3-aa96-45f3-9551-f24c39ea6cbf">CreateRequestMessage</a>, <a href="https://msdn.microsoft.com/86d031b0-2009-460b-8bed-fe7a0489f22b">CreateRetrievePendingMessage</a>, or <a href="https://msdn.microsoft.com/238a837f-4464-49ce-b87a-03abcfc0abea">CreateRetrieveCertificateMessage</a> methods.




## -see-also




<a href="https://msdn.microsoft.com/fcbac911-9e37-4994-bbb6-544b19a92749">IX509SCEPEnrollment</a>
 

 

