---
UID: NF:storprop.CdromDisableDigitalPlayback
title: CdromDisableDigitalPlayback function
author: windows-sdk-content
description: Disables digital playback for the specified CD-ROM or DVD drive.
old-location: base\cdromdisabledigitalplayback.htm
old-project: devio
ms.assetid: 289812ac-cec1-4ccc-b4ef-146b19a26ebd
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: CdromDisableDigitalPlayback, CdromDisableDigitalPlayback function, base.cdromdisabledigitalplayback, storprop/CdromDisableDigitalPlayback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: storprop.h
req.include-header: 
req.redist: 
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
 - CdromDisableDigitalPlayback
product: Windows
targetos: Windows
req.lib: 
req.dll: StorProp.dll
req.irql: 
req.product: Outlook Express 6.0
---

# CdromDisableDigitalPlayback function


## -description


Disables digital playback for the specified CD-ROM or DVD drive.


## -parameters




### -param DevInfo [in]

A handle to a device information set listing the devices for which information is to be returned. This handle is typically returned by the <a href="https://msdn.microsoft.com/31bb0fc8-0fb8-4122-b9e8-5ff8fbbd903b">SetupDiGetClassDevs</a> or <a href="https://msdn.microsoft.com/9f13ffe1-1a60-4d9a-942d-63312ca9bc5b">SetupDiGetClassDevsEx</a> function.


### -param DevInfoData [in]

A pointer to an <a href="https://msdn.microsoft.com/9ad0ef4f-4a67-4f16-8bb1-2242dad0d041">SP_DEVINFO_DATA</a> structure that defines the device instance.


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
 

 

