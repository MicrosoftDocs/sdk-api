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
 

 

