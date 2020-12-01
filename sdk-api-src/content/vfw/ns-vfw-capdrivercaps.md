---
UID: NS:vfw.tagCapDriverCaps
title: CAPDRIVERCAPS (vfw.h)
description: The CAPDRIVERCAPS structure defines the capabilities of the capture driver.An application should use the WM_CAP_DRIVER_GET_CAPS message or capDriverGetCaps macro to place a copy of the driver capabilities in a CAPDRIVERCAPS structure whenever the application connects a capture window to a capture driver.
helpviewer_keywords: ["*LPCAPDRIVERCAPS","*PCAPDRIVERCAPS","CAPDRIVERCAPS","CAPDRIVERCAPS structure [Windows Multimedia]","_win32_CAPDRIVERCAPS_str","multimedia.capdrivercaps","vfw/CAPDRIVERCAPS"]
old-location: multimedia\capdrivercaps.htm
tech.root: Multimedia
ms.assetid: 6d341be9-6b10-495b-803b-059ead1114cc
ms.date: 12/05/2018
ms.keywords: '*LPCAPDRIVERCAPS, *PCAPDRIVERCAPS, CAPDRIVERCAPS, CAPDRIVERCAPS structure [Windows Multimedia], _win32_CAPDRIVERCAPS_str, multimedia.capdrivercaps, vfw/CAPDRIVERCAPS'
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CAPDRIVERCAPS, *PCAPDRIVERCAPS, *LPCAPDRIVERCAPS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCapDriverCaps
 - vfw/tagCapDriverCaps
 - PCAPDRIVERCAPS
 - vfw/PCAPDRIVERCAPS
 - CAPDRIVERCAPS
 - vfw/CAPDRIVERCAPS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - CAPDRIVERCAPS
---

# CAPDRIVERCAPS structure


## -description

The <b>CAPDRIVERCAPS</b> structure defines the capabilities of the capture driver.

An application should use the <a href="/windows/desktop/Multimedia/wm-cap-driver-get-caps">WM_CAP_DRIVER_GET_CAPS</a> message or <a href="/windows/desktop/api/vfw/nf-vfw-capdrivergetcaps">capDriverGetCaps</a> macro to place a copy of the driver capabilities in a <b>CAPDRIVERCAPS</b> structure whenever the application connects a capture window to a capture driver.

## -struct-fields

### -field wDeviceIndex

Index of the capture driver. An index value can range from 0 to 9.

### -field fHasOverlay

Video-overlay flag. The value of this member is <b>TRUE</b> if the device supports video overlay.

### -field fHasDlgVideoSource

Video source dialog flag. The value of this member is <b>TRUE</b> if the device supports a dialog box for selecting and controlling the video source.

### -field fHasDlgVideoFormat

Video format dialog flag. The value of this member is <b>TRUE</b> if the device supports a dialog box for selecting the video format.

### -field fHasDlgVideoDisplay

Video display dialog flag. The value of this member is <b>TRUE</b> if the device supports a dialog box for controlling the redisplay of video from the capture frame buffer.

### -field fCaptureInitialized

Capture initialization flag. The value of this member is <b>TRUE</b> if a capture device has been successfully connected.

### -field fDriverSuppliesPalettes

Driver palette flag. The value of this member is <b>TRUE</b> if the driver can create palettes.

### -field hVideoIn

Not used in Win32 applications.

### -field hVideoOut

Not used in Win32 applications.

### -field hVideoExtIn

Not used in Win32 applications.

### -field hVideoExtOut

Not used in Win32 applications.

## -see-also

Video Capture



<a href="/windows/desktop/Multimedia/video-capture-structures">Video Capture Structures</a>