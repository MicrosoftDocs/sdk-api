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

# _DVD_REGION structure


## -description



Identifies the DVD region as reported by the local system components.




## -struct-fields




### -field CopySystem

Specifies whether the disk is copy protected.


### -field RegionData

Contains information about the region from the decoder.


### -field SystemRegion

Contains information about region from DVD drive.


### -field ResetCount

 




#### - Reserved

Reserved.


## -remarks



The AM_PROPERTY_DVDCOPY_REGION property uses this structure.




## -see-also




<a href="https://msdn.microsoft.com/da3abefd-8f25-449d-8787-84d2cef928da">DVD Copy Protection Property Set</a>
 

 

