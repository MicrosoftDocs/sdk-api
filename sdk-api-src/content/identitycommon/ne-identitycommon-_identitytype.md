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

# _IdentityType enumeration


## -description


Specifies the type of identities to enumerate. This enumeration is used by the <a href="https://msdn.microsoft.com/9e216959-7038-43cf-a57d-bee85d521f58">IIdentityProvider::GetIdentityEnum</a> and <a href="https://msdn.microsoft.com/df1a53e0-6296-49ed-b0f0-85e9dc9ab947">IIdentityStore::EnumerateIdentities</a> methods.


## -enum-fields




### -field IDENTITIES_ALL

Enumerate all identities.


### -field IDENTITIES_ME_ONLY

Enumerate only identities associated with the current user.

