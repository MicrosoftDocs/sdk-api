---
UID: NF:storprop.CdromEnableDigitalPlayback
title: CdromEnableDigitalPlayback function (storprop.h)
description: Enables digital playback for the specified CD-ROM or DVD drive.
helpviewer_keywords: ["CdromEnableDigitalPlayback","CdromEnableDigitalPlayback function","base.cdromenabledigitalplayback","storprop/CdromEnableDigitalPlayback"]
old-location: base\cdromenabledigitalplayback.htm
tech.root: base
ms.assetid: a50a0c9a-21f3-4d55-97c3-144f5835b6af
ms.date: 12/05/2018
ms.keywords: CdromEnableDigitalPlayback, CdromEnableDigitalPlayback function, base.cdromenabledigitalplayback, storprop/CdromEnableDigitalPlayback
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
 - CdromEnableDigitalPlayback
 - storprop/CdromEnableDigitalPlayback
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
 - CdromEnableDigitalPlayback
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

To disable digital playback for the specified CD-ROM or DVD drive, use the <a href="/windows/desktop/api/storprop/nf-storprop-cdromdisabledigitalplayback">CdromDisableDigitalPlayback</a> function. To determine whether digital playback is enabled or disabled, use the <a href="/windows/desktop/api/storprop/nf-storprop-cdromisdigitalplaybackenabled">CdromIsDigitalPlaybackEnabled</a> function.

This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to StorProp.dll.

## -see-also

<a href="/windows/desktop/api/storprop/nf-storprop-cdromdisabledigitalplayback">CdromDisableDigitalPlayback</a>



<a href="/windows/desktop/api/storprop/nf-storprop-cdromisdigitalplaybackenabled">CdromIsDigitalPlaybackEnabled</a>



<a href="/windows/desktop/api/storprop/nf-storprop-cdromknowngooddigitalplayback">CdromKnownGoodDigitalPlayback</a>



<a href="/windows/desktop/DevIO/device-management-functions">Device Management Functions</a>