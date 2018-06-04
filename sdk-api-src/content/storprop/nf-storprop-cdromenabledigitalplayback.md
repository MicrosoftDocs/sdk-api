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

# CdromEnableDigitalPlayback function


## -description


Enables digital playback for the specified CD-ROM or DVD drive.


## -parameters




### -param DevInfo [in]

A handle to a device information set listing the devices for which information is to be returned. This handle is typically returned by the <b>SetupDiGetClassDevs</b> or <b>SetupDiGetClassDevsEx</b> function.


### -param DevInfoData [in]

A pointer to an <b>SP_DEVINFO_DATA</b> structure that defines the device instance.


### -param ForceUnknown [in]

If this member is <b>TRUE</b>, playback is enabled even if the drive is not known to be good.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is an error code.




## -remarks



To disable digital playback for the specified CD-ROM or DVD drive, use the <a href="https://msdn.microsoft.com/289812ac-cec1-4ccc-b4ef-146b19a26ebd">CdromDisableDigitalPlayback</a> function. To determine whether digital playback is enabled or disabled, use the <a href="https://msdn.microsoft.com/17d1ccc6-a552-434f-84f5-471455e97dc2">CdromIsDigitalPlaybackEnabled</a> function.

This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to StorProp.dll.




## -see-also




<a href="https://msdn.microsoft.com/289812ac-cec1-4ccc-b4ef-146b19a26ebd">CdromDisableDigitalPlayback</a>



<a href="https://msdn.microsoft.com/17d1ccc6-a552-434f-84f5-471455e97dc2">CdromIsDigitalPlaybackEnabled</a>



<a href="https://msdn.microsoft.com/df242729-2082-4608-bd73-4c8d215a09ea">CdromKnownGoodDigitalPlayback</a>



<a href="https://msdn.microsoft.com/3918ba49-1549-4f0c-b9fd-303ef46b810e">Device Management Functions</a>
 

 

