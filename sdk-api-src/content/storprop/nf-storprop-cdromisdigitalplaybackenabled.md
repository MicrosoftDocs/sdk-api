---
UID: NF:storprop.CdromIsDigitalPlaybackEnabled
title: CdromIsDigitalPlaybackEnabled function
author: windows-sdk-content
description: Determines whether digital playback is enabled for the specified CD-ROM or DVD drive.
old-location: base\cdromisdigitalplaybackenabled.htm
old-project: DevIO
ms.assetid: 17d1ccc6-a552-434f-84f5-471455e97dc2
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: CdromIsDigitalPlaybackEnabled, CdromIsDigitalPlaybackEnabled function, base.cdromisdigitalplaybackenabled, storprop/CdromIsDigitalPlaybackEnabled
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MPR50_SERVICE_CHARACTERISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - StorProp.dll
api_name:
 - CdromIsDigitalPlaybackEnabled
product: Windows
targetos: Windows
req.lib: 
req.dll: StorProp.dll
req.irql: 
req.product: Outlook Express 6.0
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
 

 

