---
UID: NF:storprop.CdromKnownGoodDigitalPlayback
title: CdromKnownGoodDigitalPlayback function (storprop.h)
description: Determines whether the specified CD-ROM or DVD drive has digital playback that is known to be good.
helpviewer_keywords: ["CdromKnownGoodDigitalPlayback","CdromKnownGoodDigitalPlayback function","base.cdromknowngooddigitalplayback","storprop/CdromKnownGoodDigitalPlayback"]
old-location: base\cdromknowngooddigitalplayback.htm
tech.root: base
ms.assetid: df242729-2082-4608-bd73-4c8d215a09ea
ms.date: 12/05/2018
ms.keywords: CdromKnownGoodDigitalPlayback, CdromKnownGoodDigitalPlayback function, base.cdromknowngooddigitalplayback, storprop/CdromKnownGoodDigitalPlayback
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
req.dll: Storprop.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CdromKnownGoodDigitalPlayback
 - storprop/CdromKnownGoodDigitalPlayback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Storprop.dll
api_name:
 - CdromKnownGoodDigitalPlayback
---

# CdromKnownGoodDigitalPlayback function


## -description

Determines whether the specified CD-ROM or DVD drive has digital playback that is known to be good.

## -parameters

### -param HDevInfo [in]

A handle to a device information set listing the devices for which information is to be returned. This handle is typically returned by the <b>SetupDiGetClassDevs</b> or <b>SetupDiGetClassDevsEx</b> function.

### -param DevInfoData [in]

A pointer to an <b>SP_DEVINFO_DATA</b> structure that defines the device instance.

## -returns

If digital playback is good, the return value is <b>TRUE</b>. Otherwise, the return value is <b>FALSE</b>.

## -remarks

This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Storprop.dll.

## -see-also

<a href="/windows/desktop/DevIO/device-management-functions">Device Management Functions</a>