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

# CdromIsDigitalPlaybackEnabled function


## -description


Determines whether digital playback is enabled for the specified CD-ROM or DVD drive.


## -parameters




### -param DevInfo [in]

A handle to a device information set listing the devices for which information is to be returned. This handle is typically returned by the <b>SetupDiGetClassDevs</b> or <b>SetupDiGetClassDevsEx</b> function.


### -param DevInfoData [in]

A pointer to an <b>SP_DEVINFO_DATA</b> structure that defines the device instance.


### -param Enabled [out]

A pointer to a variable that receives <b>TRUE</b> if digital playback is enabled, and <b>FALSE</b> otherwise.


## -returns



If the function succeeds the return value is <b>ERROR_SUCCESS</b>. Otherwise, it is an error code.




## -remarks



To enable digital playback for the specified CD-ROM or DVD drive, use the <a href="https://msdn.microsoft.com/a50a0c9a-21f3-4d55-97c3-144f5835b6af">CdromEnableDigitalPlayback</a> function. To disable digital playback for the specified CD-ROM or DVD drive, use the <a href="https://msdn.microsoft.com/289812ac-cec1-4ccc-b4ef-146b19a26ebd">CdromDisableDigitalPlayback</a> function. 

This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to StorProp.dll.




## -see-also




<a href="https://msdn.microsoft.com/289812ac-cec1-4ccc-b4ef-146b19a26ebd">CdromDisableDigitalPlayback</a>



<a href="https://msdn.microsoft.com/a50a0c9a-21f3-4d55-97c3-144f5835b6af">CdromEnableDigitalPlayback</a>



<a href="https://msdn.microsoft.com/3918ba49-1549-4f0c-b9fd-303ef46b810e">Device Management Functions</a>
 

 

