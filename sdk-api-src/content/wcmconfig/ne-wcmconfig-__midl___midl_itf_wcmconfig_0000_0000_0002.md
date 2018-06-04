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

# __MIDL___MIDL_itf_wcmconfig_0000_0000_0002 enumeration


## -description


Describes the types of enumeration flags.


## -enum-fields




### -field SharedEnumeration

Describes a shared enumeration. It enumerates all namespaces that have been compiled for the machine space.


### -field UserEnumeration

Describes a user-specific  enumeration. It enumerates the namespaces that have been compiled for a specific user.


### -field AllEnumeration

A logical "OR" of shared and user enumeration.


## -remarks



<div class="alert"><b>Note</b>  UserEnumeration should not be used. No namespaces are compiled for a particular user, they are all compiled for the machine as an entity.</div>
<div> </div>


