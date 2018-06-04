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

# EALocationCodeType structure


## -description



The EALocationCodeType structure defines an Emergency Alert (EA) location code, as defined in ANSI/SCTE 28.




## -struct-fields




### -field LocationCodeScheme

Identifies the standard that shall be used to interpret the other members of this structure. Currently this value must be SCTE_18, meaning SCTE 18, "Emergency Alert Message for Cable."


### -field state_code

Contains the state_code field.


### -field county_subdivision

Contains the county_subdivision field.


### -field county_code

Contains the county_code field.


## -see-also




<a href="https://msdn.microsoft.com/5ae43ac6-519d-486b-aaa5-c766f3194ef2">BDA Structures</a>
 

 

