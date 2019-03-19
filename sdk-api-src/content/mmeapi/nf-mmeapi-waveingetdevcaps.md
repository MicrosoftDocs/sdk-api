---
UID: NF:mmeapi.waveInGetDevCaps
title: waveInGetDevCaps function (mmeapi.h)
author: windows-sdk-content
description: The waveInGetDevCaps function retrieves the capabilities of a given waveform-audio input device.
old-location: multimedia\waveingetdevcaps.htm
tech.root: Multimedia
ms.assetid: f8d4edc7-99b6-488d-974b-6fb8f0080f77
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_win32_waveInGetDevCaps, mmeapi/waveInGetDevCaps, multimedia.waveingetdevcaps, waveInGetDevCaps, waveInGetDevCaps function [Windows Multimedia]"
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
 - waveInGetDevCaps
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# waveInGetDevCaps function


## -description



The <b>waveInGetDevCaps</b> function retrieves the capabilities of a given waveform-audio input device.




## -parameters




### -param uDeviceID

Identifier of the waveform-audio output device. It can be either a device identifier or a handle of an open waveform-audio input device.


### -param pwic

Pointer to a <a href="https://msdn.microsoft.com/e96524fd-82d3-4363-989b-23fb20786f3c">WAVEINCAPS</a> structure to be filled with information about the capabilities of the device.


### -param cbwic

Size, in bytes, of the <b>WAVEINCAPS</b> structure.


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



Use this function to determine the number of waveform-audio input devices present in the system. If the value specified by the <i>uDeviceID</i> parameter is a device identifier, it can vary from zero to one less than the number of devices present. The WAVE_MAPPER constant can also be used as a device identifier. Only <i>cbwic</i> bytes (or less) of information is copied to the location pointed to by <i>pwic</i>. If <i>cbwic</i> is zero, nothing is copied and the function returns zero.




## -see-also




<a href="https://msdn.microsoft.com/3188355c-65be-4372-8e87-e7f755982592">Waveform Audio</a>



<a href="https://msdn.microsoft.com/6c8aaa54-0477-484f-91e1-d2152aa9c185">Waveform Functions</a>
 

 

