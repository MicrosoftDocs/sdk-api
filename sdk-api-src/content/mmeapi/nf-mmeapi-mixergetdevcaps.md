---
UID: NF:mmeapi.mixerGetDevCaps
title: mixerGetDevCaps function
author: windows-sdk-content
description: The mixerGetDevCaps function queries a specified mixer device to determine its capabilities.
old-location: multimedia\mixergetdevcaps.htm
tech.root: Multimedia
ms.assetid: e3403be8-f3a8-4aab-8498-0556585bc4dd
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: "_win32_mixerGetDevCaps, mixerGetDevCaps, mixerGetDevCaps function [Windows Multimedia], mixerGetDevCapsA, mixerGetDevCapsW, mmeapi/mixerGetDevCaps, mmeapi/mixerGetDevCapsA, mmeapi/mixerGetDevCapsW, multimedia.mixergetdevcaps"
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
req.unicode-ansi: mixerGetDevCapsW (Unicode) and mixerGetDevCapsA (ANSI)
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
 - API-MS-Win-mm-mme-l1-1-0.dll
 - winmmbase.dll
api_name:
 - mixerGetDevCaps
 - mixerGetDevCapsA
 - mixerGetDevCapsW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- mixerGetDevCaps
: 
---

# mixerGetDevCaps function


## -description



The <b>mixerGetDevCaps</b> function queries a specified mixer device to determine its capabilities.




## -parameters




### -param uMxId

Identifier or handle of an open mixer device.


### -param pmxcaps

Pointer to a <a href="https://msdn.microsoft.com/4a4220cb-fdb1-4afe-821f-27f5adb51530">MIXERCAPS</a> structure that receives information about the capabilities of the device.


### -param cbmxcaps

Size, in bytes, of the <a href="https://msdn.microsoft.com/4a4220cb-fdb1-4afe-821f-27f5adb51530">MIXERCAPS</a> structure.


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
The specified device identifier is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALHANDLE</b></dt>
</dl>
</td>
<td width="60%">
The mixer device handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALPARAM</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>
 




## -remarks



Use the <a href="https://msdn.microsoft.com/ae3c3a28-1dc1-4e35-99d6-68e629124a89">mixerGetNumDevs</a> function to determine the number of mixer devices present in the system. The device identifier specified by <i>uMxId</i> varies from zero to one less than the number of mixer devices present.

Only the number of bytes (or less) of information specified in <i>cbmxcaps</i> is copied to the location pointed to by <i>pmxcaps</i>. If <i>cbmxcaps</i> is zero, nothing is copied, and the function returns successfully.

This function also accepts a mixer device handle returned by the <a href="https://msdn.microsoft.com/7977680b-0967-4b85-9926-fc2725681de9">mixerOpen</a> function as the <i>uMxId</i> parameter. The application should cast the <b>HMIXER</b> handle to a <b>UINT</b>.




## -see-also




<a href="https://msdn.microsoft.com/19f53a98-1a01-4954-a5d7-c428aa2bfa38">Audio Mixer Functions</a>



<a href="https://msdn.microsoft.com/7489fcac-fd4c-46cf-8a1a-e4de576974f0">Audio Mixers</a>
 

 

