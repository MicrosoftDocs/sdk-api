---
UID: NF:storprop.CdromDisableDigitalPlayback
title: CdromDisableDigitalPlayback function (storprop.h)
description: Disables digital playback for the specified CD-ROM or DVD drive.
helpviewer_keywords: ["CdromDisableDigitalPlayback","CdromDisableDigitalPlayback function","base.cdromdisabledigitalplayback","storprop/CdromDisableDigitalPlayback"]
old-location: base\cdromdisabledigitalplayback.htm
tech.root: base
ms.assetid: 289812ac-cec1-4ccc-b4ef-146b19a26ebd
ms.date: 12/05/2018
ms.keywords: CdromDisableDigitalPlayback, CdromDisableDigitalPlayback function, base.cdromdisabledigitalplayback, storprop/CdromDisableDigitalPlayback
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
 - CdromDisableDigitalPlayback
 - storprop/CdromDisableDigitalPlayback
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
 - CdromDisableDigitalPlayback
---

# CdromDisableDigitalPlayback function


## -description

Disables digital playback for the specified CD-ROM or DVD drive.

## -parameters

### -param DevInfo [in]

A handle to a device information set listing the devices for which information is to be returned. This handle is typically returned by the <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassdevsw">SetupDiGetClassDevs</a> or <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassdevsexa">SetupDiGetClassDevsEx</a> function.

### -param DevInfoData [in]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that defines the device instance.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is an error code.

## -remarks

To enable digital playback for the specified CD-ROM or DVD drive, use the <a href="/windows/desktop/api/storprop/nf-storprop-cdromenabledigitalplayback">CdromEnableDigitalPlayback</a> function. To determine whether digital playback is enabled or disabled, use the <a href="/windows/desktop/api/storprop/nf-storprop-cdromisdigitalplaybackenabled">CdromIsDigitalPlaybackEnabled</a> function.

This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to StorProp.dll.

## -see-also

<a href="/windows/desktop/api/storprop/nf-storprop-cdromenabledigitalplayback">CdromEnableDigitalPlayback</a>



<a href="/windows/desktop/api/storprop/nf-storprop-cdromisdigitalplaybackenabled">CdromIsDigitalPlaybackEnabled</a>



<a href="/windows/desktop/DevIO/device-management-functions">Device Management Functions</a>