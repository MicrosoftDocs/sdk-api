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

# __MIDL___MIDL_itf_wrdsgraphicschannels_0000_0002_0001 enumeration


## -description


Used to specify the type of graphics virtual channel to create in the <a href="https://msdn.microsoft.com/2dcce4ac-aa1d-4bdf-9c95-8737f924d0e9">IWRdsGraphicsChannelManager::CreateChannel</a> method.


## -enum-fields




### -field WRdsGraphicsChannelType_GuaranteedDelivery

The channel delivery must be guaranteed.


### -field WRdsGraphicsChannelType_BestEffortDelivery

The channel delivery can be lossy.


## -see-also




<a href="https://msdn.microsoft.com/2dcce4ac-aa1d-4bdf-9c95-8737f924d0e9">IWRdsGraphicsChannelManager::CreateChannel</a>
 

 

