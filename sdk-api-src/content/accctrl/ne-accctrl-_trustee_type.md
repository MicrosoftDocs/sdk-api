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

# _TRUSTEE_TYPE enumeration


## -description


The <b>TRUSTEE_TYPE</b> enumeration contains values that indicate the type of trustee identified by a 
<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure.


## -enum-fields




### -field TRUSTEE_IS_UNKNOWN

The trustee type is unknown, but it may be valid.


### -field TRUSTEE_IS_USER

Indicates a user.


### -field TRUSTEE_IS_GROUP

Indicates a group.


### -field TRUSTEE_IS_DOMAIN

Indicates a domain.


### -field TRUSTEE_IS_ALIAS

Indicates an alias.


### -field TRUSTEE_IS_WELL_KNOWN_GROUP

Indicates a 
<a href="https://msdn.microsoft.com/eb2f95c4-9465-409b-b76c-9ccae1d05eda">well-known group</a>.


### -field TRUSTEE_IS_DELETED

Indicates a deleted account.


### -field TRUSTEE_IS_INVALID

Indicates a trustee type that is not valid.


### -field TRUSTEE_IS_COMPUTER

Indicates a computer.


## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="https://msdn.microsoft.com/e2f22838-102e-432c-9c82-06a3e0741374">Authorization Enumerations</a>



<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a>
 

 

