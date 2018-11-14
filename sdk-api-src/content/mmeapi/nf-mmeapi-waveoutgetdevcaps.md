---
UID: NF:mmeapi.waveOutGetDevCaps
title: waveOutGetDevCaps function
author: windows-sdk-content
description: The waveOutGetDevCaps function retrieves the capabilities of a given waveform-audio output device.
old-location: multimedia\waveoutgetdevcaps.htm
tech.root: Multimedia
ms.assetid: 294daf81-d52a-44b4-b22a-d75ad6e05fee
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: "_win32_waveOutGetDevCaps, mmeapi/waveOutGetDevCaps, multimedia.waveoutgetdevcaps, waveOutGetDevCaps, waveOutGetDevCaps function [Windows Multimedia]"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winmm.dll
api_name:
 - waveOutGetDevCaps
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- waveOutGetDevCaps
: 
---

# waveOutGetDevCaps function


## -description



The <b>waveOutGetDevCaps</b> function retrieves the capabilities of a given waveform-audio output device.




## -parameters




### -param uDeviceID

Identifier of the waveform-audio output device. It can be either a device identifier or a handle of an open waveform-audio output device.


### -param pwoc

Pointer to a <a href="https://msdn.microsoft.com/756f47fa-c0d1-4729-a0f6-096a1212d0a2">WAVEOUTCAPS</a> structure to be filled with information about the capabilities of the device.


### -param cbwoc

Size, in bytes, of the <b>WAVEOUTCAPS</b> structure.


## -returns



Returns MMSYSERR_NOERROR if successful or an error otherwise. Possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_BADDEVICEID</b></dt>
</dl>
</td>
<td width="60%">
Specified device identifier is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_NODRIVER</b></dt>
</dl>
</td>
<td width="60%">
No device driver is present.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_NOMEM</b></dt>
</dl>
</td>
<td width="60%">
Unable to allocate or lock memory.

</td>
</tr>
</table>
 




## -remarks



Use the <b>waveOutGetNumDevs</b> function to determine the number of waveform-audio output devices present in the system. If the value specified by the <i>uDeviceID</i> parameter is a device identifier, it can vary from zero to one less than the number of devices present. The WAVE_MAPPER constant can also be used as a device identifier. Only <i>cbwoc</i> bytes (or less) of information is copied to the location pointed to by <i>pwoc</i>. If <i>cbwoc</i> is zero, nothing is copied and the function returns zero.




## -see-also




<a href="https://msdn.microsoft.com/3188355c-65be-4372-8e87-e7f755982592">Waveform Audio</a>



<a href="https://msdn.microsoft.com/6c8aaa54-0477-484f-91e1-d2152aa9c185">Waveform Functions</a>
 

 

