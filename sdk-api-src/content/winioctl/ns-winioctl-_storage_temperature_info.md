---
UID: NS:winioctl._STORAGE_TEMPERATURE_INFO
title: "_STORAGE_TEMPERATURE_INFO"
author: windows-sdk-content
description: Describes device temperature data. Returned as part of STORAGE_TEMPERATURE_DATA_DESCRIPTOR when querying for temperature data with an IOCTL_STORAGE_QUERY_PROPERTY request.
old-location: fs\storage_temperature_info.htm
tech.root: fileio
ms.assetid: 236B4AC7-AF5E-4556-9FFD-D64C450E6492
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: "*PSTORAGE_TEMPERATURE_INFO, PSTORAGE_TEMPERATURE_INFO, PSTORAGE_TEMPERATURE_INFO structure pointer [Files], STORAGE_TEMPERATURE_INFO, STORAGE_TEMPERATURE_INFO structure [Files], _STORAGE_TEMPERATURE_INFO, fs.storage_temperature_info, winioctl/PSTORAGE_TEMPERATURE_INFO, winioctl/STORAGE_TEMPERATURE_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoctl.h
api_name:
 - STORAGE_TEMPERATURE_INFO
product: Windows
targetos: Windows
req.typenames: STORAGE_TEMPERATURE_INFO, *PSTORAGE_TEMPERATURE_INFO
req.redist: 
---

# _STORAGE_TEMPERATURE_INFO structure


## -description


Describes  device temperature data. Returned as part of <a href="https://msdn.microsoft.com/E155B31F-6543-42E3-BCAB-B1B0100D23E4">STORAGE_TEMPERATURE_DATA_DESCRIPTOR</a> when querying for temperature data with an <a href="https://msdn.microsoft.com/6755dcd4-e4a0-423f-9dcc-b9719c8e5c88">IOCTL_STORAGE_QUERY_PROPERTY</a> request. 


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

Indicates if <i>OverThreshold</i> can be changed by using <a href="https://msdn.microsoft.com/6B4BF202-6CC9-4571-9078-019984805F00">IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD</a>.


### -field UnderThresholdChangable

Indicates if <i>UnderThreshold</i> can be changed by using <a href="https://msdn.microsoft.com/6B4BF202-6CC9-4571-9078-019984805F00">IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD</a>.


### -field EventGenerated

Indicates if a notification will be generated when the current temperature crosses a threshold.


### -field Reserved0

Reserved for future use.


### -field Reserved1

Reserved for future use.


## -see-also




<a href="https://msdn.microsoft.com/6755dcd4-e4a0-423f-9dcc-b9719c8e5c88">IOCTL_STORAGE_QUERY_PROPERTY</a>



<a href="https://msdn.microsoft.com/6B4BF202-6CC9-4571-9078-019984805F00">IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD</a>



<a href="https://msdn.microsoft.com/9747be01-7c70-4697-97f7-e3830b54ba0a">STORAGE_PROPERTY_ID</a>



<a href="https://msdn.microsoft.com/c97a14ab-628c-41f1-96c3-0f47654d0606">STORAGE_PROPERTY_QUERY</a>
 

 

