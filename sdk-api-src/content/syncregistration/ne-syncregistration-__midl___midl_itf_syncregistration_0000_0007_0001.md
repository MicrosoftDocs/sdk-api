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

# __MIDL___MIDL_itf_syncregistration_0000_0007_0001 enumeration


## -description


Represents the different types of synchronization registration events.


## -enum-fields




### -field SRE_PROVIDER_ADDED

A synchronization provider registration has been added.


### -field SRE_PROVIDER_REMOVED

A synchronization provider registration has been removed.


### -field SRE_PROVIDER_UPDATED

The property store (represented by the <b>IPropertyStore</b> interface) of a synchronization provider or a synchronization provider configuration UI has changed.


### -field SRE_PROVIDER_STATE_CHANGED

The synchronization provider state has changed.


### -field SRE_CONFIGUI_ADDED

A synchronization provider configuration UI has been added.


### -field SRE_CONFIGUI_REMOVED

A synchronization provider configuration UI has been removed.


### -field SRE_CONFIGUI_UPDATED

A synchronization provider configuration UI has been updated.


## -see-also




<a href="https://msdn.microsoft.com/efd6d871-8c1a-4653-b8a5-9e2d8872c499">Windows Sync Registration Enumerations</a>
 

 

