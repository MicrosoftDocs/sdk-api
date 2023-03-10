---
UID: NF:storprop.CdromIsDigitalPlaybackEnabled
title: CdromIsDigitalPlaybackEnabled function (storprop.h)
description: Determines whether digital playback is enabled for the specified CD-ROM or DVD drive.
helpviewer_keywords: ["CdromIsDigitalPlaybackEnabled","CdromIsDigitalPlaybackEnabled function","base.cdromisdigitalplaybackenabled","storprop/CdromIsDigitalPlaybackEnabled"]
old-location: base\cdromisdigitalplaybackenabled.htm
tech.root: base
ms.assetid: 17d1ccc6-a552-434f-84f5-471455e97dc2
ms.date: 12/05/2018
ms.keywords: CdromIsDigitalPlaybackEnabled, CdromIsDigitalPlaybackEnabled function, base.cdromisdigitalplaybackenabled, storprop/CdromIsDigitalPlaybackEnabled
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CdromIsDigitalPlaybackEnabled
 - storprop/CdromIsDigitalPlaybackEnabled
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - StorProp.dll
api_name:
 - CdromIsDigitalPlaybackEnabled
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

To enable digital playback for the specified CD-ROM or DVD drive, use the <a href="/windows/desktop/api/storprop/nf-storprop-cdromenabledigitalplayback">CdromEnableDigitalPlayback</a> function. To disable digital playback for the specified CD-ROM or DVD drive, use the <a href="/windows/desktop/api/storprop/nf-storprop-cdromdisabledigitalplayback">CdromDisableDigitalPlayback</a> function. 

This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to StorProp.dll.

## -see-also

<a href="/windows/desktop/api/storprop/nf-storprop-cdromdisabledigitalplayback">CdromDisableDigitalPlayback</a>



<a href="/windows/desktop/api/storprop/nf-storprop-cdromenabledigitalplayback">CdromEnableDigitalPlayback</a>



<a href="/windows/desktop/DevIO/device-management-functions">Device Management Functions</a>