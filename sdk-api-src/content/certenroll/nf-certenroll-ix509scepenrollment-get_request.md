---
UID: NF:certenroll.IX509SCEPEnrollment.get_Request
title: IX509SCEPEnrollment::get_Request method
author: windows-driver-content
description: Gets the inner PKCS10 request.
old-location: security\ix509scepenrollment_request.htm
old-project: SecCertEnroll
ms.assetid: 9446cd62-5a02-4701-8b13-9e46508fbfaa
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: IX509SCEPEnrollment, IX509SCEPEnrollment interface [Security], Request property, IX509SCEPEnrollment.Request, IX509SCEPEnrollment::get_Request, Request property [Security], Request property [Security], IX509SCEPEnrollment interface, certenroll/IX509SCEPEnrollment::Request, certenroll/IX509SCEPEnrollment::get_Request, get_Request,IX509SCEPEnrollment.get_Request, security.ix509scepenrollment_request
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
-	IX509SCEPEnrollment.Request
-	IX509SCEPEnrollment.get_Request
product: Windows
targetos: Windows
req.lib: 
req.dll: Certenroll.dll
req.irql: 
---

# IX509SCEPEnrollment::get_Request method


## -description


Gets the inner PKCS10 request.

This property is read-only.


## -parameters


## -remarks



You can use the inner PKCS10 request instance to set the subject, extensions, private key properties, encryption algorithm and strength, and the hash algorithm before you call the <a href="https://msdn.microsoft.com/b86d6dc3-aa96-45f3-9551-f24c39ea6cbf">CreateRequestMessage</a> method.




## -see-also




<a href="https://msdn.microsoft.com/fcbac911-9e37-4994-bbb6-544b19a92749">IX509SCEPEnrollment</a>
 

 

