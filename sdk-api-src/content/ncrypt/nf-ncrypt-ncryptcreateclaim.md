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

# NCryptCreateClaim function


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Creates a key attestation claim.


## -parameters




### -param hSubjectKey [in]

The subject key handle that the claim is created for.


### -param hAuthorityKey [in, optional]

The authority key handle that the claim is based on.


### -param dwClaimType [in]

The type of claim.


### -param pParameterList [in, optional]

An optional parameter list.


### -param pbClaimBlob [out]

Output of the created claim blob.


### -param cbClaimBlob [in]


### -param pcbResult [out]

The output of the created claim blob.


### -param dwFlags [in]

As of Windows 10, no  flags are defined. This parameter should be set to 0.


## -returns



Returns a status code that indicates the success or failure of the function.



