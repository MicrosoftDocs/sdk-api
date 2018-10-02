---
UID: NF:storprop.CdromEnableDigitalPlayback
title: CdromEnableDigitalPlayback function
author: windows-sdk-content
description: Enables digital playback for the specified CD-ROM or DVD drive.
old-location: base\cdromenabledigitalplayback.htm
tech.root: devio
ms.assetid: a50a0c9a-21f3-4d55-97c3-144f5835b6af
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: CdromEnableDigitalPlayback, CdromEnableDigitalPlayback function, base.cdromenabledigitalplayback, storprop/CdromEnableDigitalPlayback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: storprop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
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
req.dll: StorProp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - StorProp.dll
api_name:
 - CdromEnableDigitalPlayback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

