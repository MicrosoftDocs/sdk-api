---
UID: NF:mmeapi.waveInGetDevCaps
title: waveInGetDevCaps function (mmeapi.h)
description: The waveInGetDevCaps function retrieves the capabilities of a given waveform-audio input device.
helpviewer_keywords: ["_win32_waveInGetDevCaps","mmeapi/waveInGetDevCaps","multimedia.waveingetdevcaps","waveInGetDevCaps","waveInGetDevCaps function [Windows Multimedia]"]
old-location: multimedia\waveingetdevcaps.htm
tech.root: Multimedia
ms.assetid: f8d4edc7-99b6-488d-974b-6fb8f0080f77
ms.date: 12/05/2018
ms.keywords: _win32_waveInGetDevCaps, mmeapi/waveInGetDevCaps, multimedia.waveingetdevcaps, waveInGetDevCaps, waveInGetDevCaps function [Windows Multimedia]
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
 - waveInGetDevCaps
 - mmeapi/waveInGetDevCaps
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
 - waveInGetDevCaps
---

# waveInGetDevCaps function


## -description

The <b>waveInGetDevCaps</b> function retrieves the capabilities of a given waveform-audio input device.

## -parameters

### -param uDeviceID

Identifier of the waveform-audio input device. It can be either a device identifier or a handle of an open waveform-audio input device.

### -param pwic

Pointer to a [WAVEINCAPS](ns-mmeapi-waveincaps.md) structure to be filled with information about the capabilities of the device.

### -param cbwic

Size, in bytes, of the **WAVEINCAPS** structure.

## -returns

Returns MMSYSERR_NOERROR if successful or an error otherwise. Possible error values include the following.


| Return code | Description |
|-------------|-------------|
| MMSYSERR_BADDEVICEID | Specified device identifier is out of range. |
| MMSYSERR_NODRIVER | No device driver is present. |
| MMSYSERR_NOMEM | Unable to allocate or lock memory. |


## -remarks

Use this function to determine the number of waveform-audio input devices present in the system. If the value specified by the *uDeviceID* parameter is a device identifier, it can vary from zero to one less than the number of devices present. The WAVE_MAPPER constant can also be used as a device identifier. Only *cbwic* bytes (or less) of information is copied to the location pointed to by *pwic*. If *cbwic* is zero, nothing is copied and the function returns zero.

## -see-also

[Waveform Audio](/windows/desktop/Multimedia/waveform-audio)
[Waveform Functions](/windows/desktop/Multimedia/waveform-functions)