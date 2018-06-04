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

# CdromDisableDigitalPlayback function


## -description


Disables digital playback for the specified CD-ROM or DVD drive.


## -parameters




### -param DevInfo [in]

A handle to a device information set listing the devices for which information is to be returned. This handle is typically returned by the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551069">SetupDiGetClassDevs</a> or <a href="https://msdn.microsoft.com/library/windows/hardware/ff551072">SetupDiGetClassDevsEx</a> function.


### -param DevInfoData [in]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552344">SP_DEVINFO_DATA</a> structure that defines the device instance.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is an error code.




## -remarks



To enable digital playback for the specified CD-ROM or DVD drive, use the <a href="https://msdn.microsoft.com/a50a0c9a-21f3-4d55-97c3-144f5835b6af">CdromEnableDigitalPlayback</a> function. To determine whether digital playback is enabled or disabled, use the <a href="https://msdn.microsoft.com/17d1ccc6-a552-434f-84f5-471455e97dc2">CdromIsDigitalPlaybackEnabled</a> function.

This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to StorProp.dll.




## -see-also




<a href="https://msdn.microsoft.com/a50a0c9a-21f3-4d55-97c3-144f5835b6af">CdromEnableDigitalPlayback</a>



<a href="https://msdn.microsoft.com/17d1ccc6-a552-434f-84f5-471455e97dc2">CdromIsDigitalPlaybackEnabled</a>



<a href="https://msdn.microsoft.com/3918ba49-1549-4f0c-b9fd-303ef46b810e">Device Management Functions</a>
 

 

