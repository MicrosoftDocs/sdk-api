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

# _CLAIM_SECURITY_ATTRIBUTES_INFORMATION structure


## -description


The <b>CLAIM_SECURITY_ATTRIBUTES_INFORMATION</b> structure defines the security attributes for the claim. 


## -struct-fields




### -field Version

The version of the security attribute. This must be CLAIM_SECURITY_ATTRIBUTES_INFORMATION_VERSION_V1.


### -field Reserved

This member is currently reserved and must be zero when setting an attribute and is ignored when getting an attribute.


### -field AttributeCount

The number of values.


### -field Attribute

The actual attribute.


### -field Attribute.pAttributeV1

Pointer to an array that contains the <b>AttributeCount</b> member of the <a href="https://msdn.microsoft.com/FDBB9B00-01C3-474A-81FF-97C5CBA3261B">CLAIM_SECURITY_ATTRIBUTE_V1</a> structure.

