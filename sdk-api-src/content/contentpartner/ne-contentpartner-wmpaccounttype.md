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

# WMPAccountType enumeration


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>WMPAccountType</b> enumeration defines account types for an online store.




## -enum-fields




### -field wmpatBuyOnly

The user is only authorized to purchase content.


### -field wmpatSubscription

The user has a subscription account, but content must be purchased to synchronize to a device based on Windows Media DRM for Portable Devices.


### -field wmpatJanus

The user has a subscription account and the subscription content can be synchronized to a device based on Windows Media DRM for Portable Devices.


## -see-also




<a href="https://msdn.microsoft.com/7359585f-6e8f-498f-a5a2-230265bae147">Enumerations for Type 1 Online Stores</a>



<a href="https://msdn.microsoft.com/ca63b65c-9a60-4c5d-a9f2-69d1168c53a5">IWMPContentPartner::GetContentPartnerInfo</a>
 

 

