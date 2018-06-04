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

# _STORAGE_PHYSICAL_ADAPTER_DATA structure


## -description


Describes a physical storage adapter.


## -struct-fields




### -field AdapterId

Specifies the adapter ID.


### -field HealthStatus

A <a href="https://msdn.microsoft.com/library/windows/hardware/mt653957">STORAGE_COMPONENT_HEALTH_STATUS</a>-typed value. 


### -field CommandProtocol

A <a href="https://msdn.microsoft.com/library/windows/hardware/dn931818">STORAGE_PROTOCOL_TYPE</a>-typed value.


### -field SpecVersion

A <a href="https://msdn.microsoft.com/library/windows/hardware/mt653963">STORAGE_SPEC_VERSION</a>-typed value that specifies the supported storage spec version (for example, AHCI 1.3.1).


### -field Vendor

 


### -field Model

 


### -field FirmwareRevision

 


### -field PhysicalLocation

 


### -field ExpanderConnected

Indicates whether an expander is connected.


### -field Reserved0

 


### -field Reserved1

 




#### - FirmwareRevision[16]

Specifies the firmware revision.


#### - Model[40]

Specifies the adapter model.


#### - PhysicalLocation[32]

Reserved for future use.


#### - Reserved0[3]

Reserved.


#### - Reserved1[3]

Reserved.


#### - Vendor[8]

Specifies the adapter vendor.

