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

# _SILO_INFO structure


## -description


The <b>SILO_INFO</b> structure contains information that identifies and describes the silo.


## -struct-fields




### -field ulSTID

Silo Type Identifier for the silo assigned by IEEE 1667 Working Group.


### -field SpecificationMajor

Major version of the specification implemented in the silo.


### -field SpecificationMinor

Minor version of the specification implemented in the silo.


### -field ImplementationMajor

Major version of the firmware implemented in the silo.


### -field ImplementationMinor

Minor version of the firmware implemented in the silo.


### -field type

Type of the silo.


### -field capabilities

Capabilities of the silo.

