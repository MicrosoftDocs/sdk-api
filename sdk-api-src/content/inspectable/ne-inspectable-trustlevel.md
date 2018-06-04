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

# TrustLevel enumeration


## -description


Represents the trust level of an activatable class.


## -enum-fields




### -field BaseTrust

The component has access to resources that are not protected.


### -field PartialTrust

The component has access to resources requested in the app manifest and approved by the user.


### -field FullTrust

The component requires the full privileges of the user.


## -remarks



Classes can be activated depending on the trust level of the caller and the trust classification of the activatable class.




## -see-also




<a href="https://msdn.microsoft.com/E7E8AFD1-A8B7-4023-9F8B-573E0D2622F6">IInspectable::GetTrustLevel</a>
 

 

