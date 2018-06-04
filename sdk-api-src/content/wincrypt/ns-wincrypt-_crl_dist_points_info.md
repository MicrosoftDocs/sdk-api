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

# _CRL_DIST_POINTS_INFO structure


## -description


The <b>CRL_DIST_POINTS_INFO</b> structure contains a list of <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL) distribution points a certificate user can reference to determine whether the certificate has been revoked.


## -struct-fields




### -field cDistPoint

Number of elements in the <b>rgDistPoint</b> member array.


### -field rgDistPoint

Array of 
<a href="https://msdn.microsoft.com/ec7ccc54-0aaa-4c32-8aa1-dcbaf59f9991">CRL_DIST_POINT</a> structures.


## -see-also




<a href="https://msdn.microsoft.com/ec7ccc54-0aaa-4c32-8aa1-dcbaf59f9991">CRL_DIST_POINT</a>
 

 

