---
UID: NF:mmeapi.waveOutGetDevCaps
title: waveOutGetDevCaps function (mmeapi.h)
description: The waveOutGetDevCaps function retrieves the capabilities of a given waveform-audio output device.
helpviewer_keywords: ["_win32_waveOutGetDevCaps","mmeapi/waveOutGetDevCaps","multimedia.waveoutgetdevcaps","waveOutGetDevCaps","waveOutGetDevCaps function [Windows Multimedia]"]
old-location: multimedia\waveoutgetdevcaps.htm
tech.root: Multimedia
ms.assetid: 294daf81-d52a-44b4-b22a-d75ad6e05fee
ms.date: 12/05/2018
ms.keywords: _win32_waveOutGetDevCaps, mmeapi/waveOutGetDevCaps, multimedia.waveoutgetdevcaps, waveOutGetDevCaps, waveOutGetDevCaps function [Windows Multimedia]
req.header: mmeapi.h
req.include-header: Windows.h
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
req.lib: Winmm.lib
req.dll: Winmm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - waveOutGetDevCaps
 - mmeapi/waveOutGetDevCaps
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winmm.dll
api_name:
 - waveOutGetDevCaps
---

# waveOutGetDevCaps function


## -description

The **waveOutGetDevCaps** function retrieves the capabilities of a given waveform-audio output device.

## -parameters

### -param uDeviceID

Identifier of the waveform-audio output device. It can be either a device identifier or a handle of an open waveform-audio output device.

### -param pwoc

Pointer to a [WAVEOUTCAPS](ns-mmeapi-waveoutcaps.md) structure to be filled with information about the capabilities of the device.

### -param cbwoc

Size, in bytes, of the **WAVEOUTCAPS** structure.

## -returns

Returns MMSYSERR_NOERROR if successful or an error otherwise. Possible error values include the following.

| Return code | Description |
|-------------|-------------|
| **MMSYSERR_BADDEVICEID** | Specified device identifier is out of range. |
| **MMSYSERR_NODRIVER** | No device driver is present. |
| **MMSYSERR_NOMEM** | Unable to allocate or lock memory. |

## -remarks

Use the **waveOutGetNumDevs** function to determine the number of waveform-audio output devices present in the system. If the value specified by the *uDeviceID* parameter is a device identifier, it can vary from zero to one less than the number of devices present. The WAVE_MAPPER constant can also be used as a device identifier. Only *cbwoc* bytes (or less) of information is copied to the location pointed to by *pwoc*. If *cbwoc* is zero, nothing is copied and the function returns zero.

## -see-also

[Waveform Audio](/windows/desktop/Multimedia/waveform-audio)



[Waveform Functions](/windows/desktop/Multimedia/waveform-functions)