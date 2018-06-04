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

# _CMC_TAGGED_REQUEST structure


## -description


The <b>CMC_TAGGED_REQUEST</b> structure is used in the 
<a href="https://msdn.microsoft.com/6245af5a-7a19-4665-bf6c-ad803998d840">CMC_DATA_INFO</a> structures to request a certificate. In the future, it may be used for other requests.


## -struct-fields




### -field dwTaggedRequestChoice

<b>DWORD</b> identifying the union member to be used. CMC_TAGGED_CERT_REQUEST_CHOICE can be used to select the CMC_TAGGED_CERT_REQUEST.


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.pTaggedCertRequest

A pointer to a 
<a href="https://msdn.microsoft.com/a90ec8c8-bda5-47a8-a1bb-f70f2eda01b7">CMC_TAGGED_CERT_REQUEST</a> structure containing the signed <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a>.


## -remarks



Additional members of the union may be defined in future versions.



