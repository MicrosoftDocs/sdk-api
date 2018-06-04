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

# X509SCEPFailInfo enumeration


## -description


The <b>X509SCEPFailInfo</b> enumeration   describes the nature of an SCEP certificate enrollment failure. This enumeration is used by the <a href="https://msdn.microsoft.com/fcbac911-9e37-4994-bbb6-544b19a92749">IX509SCEPEnrollment</a> interface.


## -enum-fields




### -field SCEPFailUnknown


### -field SCEPFailBadAlgorithm

Failure due to an unrecognized or unsupported algorithm.


### -field SCEPFailBadMessageCheck

The integrity check failed.


### -field SCEPFailBadRequest

The transaction was not permitted or was not supported.


### -field SCEPFailBadTime

The signing time attribute from the PKCS7 authenticated attributes was not sufficiently close to the system time.


### -field SCEPFailBadCertId

No certificate could be identified.


## -see-also




<a href="https://msdn.microsoft.com/4fd76b7e-8b19-46da-b352-7668917a6585">FailInfo</a>
 

 

