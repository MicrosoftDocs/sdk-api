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

# _STORAGE_TEMPERATURE_INFO structure


## -description


Describes  device temperature data. Returned as part of <a href="https://msdn.microsoft.com/library/windows/hardware/mt651017">STORAGE_TEMPERATURE_DATA_DESCRIPTOR</a> when querying for temperature data with an <a href="https://msdn.microsoft.com/library/windows/hardware/ff560590">IOCTL_STORAGE_QUERY_PROPERTY</a> request. 


## -struct-fields




### -field Index

Identifies the instance of temperature information. Starts from 0. Index 0 may indicate a composite value.      


### -field Temperature

A signed value that indicates the current temperature, in degrees Celsius. 


### -field OverThreshold

A signed value that specifies the maximum temperature within the desired threshold, in degrees Celsius.


### -field UnderThreshold

A signed value that specifies the minimum temperature within the desired threshold, in degrees Celsius.


### -field OverThresholdChangable

Indicates if <i>OverThreshold</i> can be changed by using <a href="https://msdn.microsoft.com/library/windows/hardware/mt650982">IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD</a>.


### -field UnderThresholdChangable

Indicates if <i>UnderThreshold</i> can be changed by using <a href="https://msdn.microsoft.com/library/windows/hardware/mt650982">IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD</a>.


### -field EventGenerated

Indicates if a notification will be generated when the current temperature crosses a threshold.


### -field Reserved0

Reserved for future use.


### -field Reserved1

Reserved for future use.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff560590">IOCTL_STORAGE_QUERY_PROPERTY</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt650982">IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566996">STORAGE_PROPERTY_ID</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566997">STORAGE_PROPERTY_QUERY</a>
 

 

