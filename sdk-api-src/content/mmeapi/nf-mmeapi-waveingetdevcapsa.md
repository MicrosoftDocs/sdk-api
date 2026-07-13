---
UID: NF:mmeapi.waveInGetDevCapsA
tech.root: Multimedia
title: waveInGetDevCapsA
ms.date: 10/28/2025
targetos: Windows
description: The waveInGetDevCapsA function retrieves the capabilities of a given waveform-audio input device. (ANSI)
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Winmm.dll
req.header: mmeapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Winmm.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 2000 Professional
req.target-min-winversvr: Windows 2000 Server
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - mmeapi.h
api_name:
 - waveInGetDevCapsA
f1_keywords:
 - waveInGetDevCapsA
 - mmeapi/waveInGetDevCapsA
dev_langs:
 - c++
helpviewer_keywords:
 - waveInGetDevCapsA
---

## -description

The **waveInGetDevCapsA** function retrieves the capabilities of a given waveform-audio input device. This is the ANSI version of this function.

## -parameters

### -param uDeviceID

Identifier of the waveform-audio input device. It can be either a device identifier or a handle of an open waveform-audio input device.

### -param pwic

Pointer to a [WAVEINCAPSA](ns-mmeapi-waveincapsa.md) structure to be filled with information about the capabilities of the device.

### -param cbwic

Size, in bytes, of the **WAVEINCAPSA** structure.

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

