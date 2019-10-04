---
UID: NF:mmeapi.auxGetDevCapsA
title: auxGetDevCapsA function (mmeapi.h)
author: windows-sdk-content
description: The auxGetDevCaps function retrieves the capabilities of a given auxiliary output device.
old-location: multimedia\auxgetdevcaps.htm
tech.root: Multimedia
ms.assetid: c0920425-fb42-4112-b0c1-f4b607b9e794
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_win32_auxGetDevCaps, auxGetDevCaps, auxGetDevCaps function [Windows Multimedia], auxGetDevCapsA, auxGetDevCapsW, mmeapi/auxGetDevCaps, mmeapi/auxGetDevCapsA, mmeapi/auxGetDevCapsW, multimedia.auxgetdevcaps"
ms.topic: function
f1_keywords: 
 - "mmeapi/auxGetDevCaps"
dev_langs:
 - c++
req.header: mmeapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: auxGetDevCapsW (Unicode) and auxGetDevCapsA (ANSI)
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
 - auxGetDevCaps
 - auxGetDevCapsA
 - auxGetDevCapsW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# auxGetDevCapsA function


## -description



The <b>auxGetDevCaps</b> function retrieves the capabilities of a given auxiliary output device.




## -parameters




### -param uDeviceID

Identifier of the auxiliary output device to be queried. Specify a valid device identifier (see the following comments section), or use the following constant:

<table>
<tr>
<th>Value
</th>
<th>Meaning
</th>
</tr>
<tr>
<td>AUX_MAPPER</td>
<td>Auxiliary audio mapper. The function returns an error if no auxiliary audio mapper is installed.</td>
</tr>
</table>
 


### -param pac

Pointer to an <a href="https://docs.microsoft.com/previous-versions/dd756711(v=vs.85)">AUXCAPS</a> structure to be filled with information about the capabilities of the device.


### -param cbac

Size, in bytes, of the <a href="https://docs.microsoft.com/previous-versions/dd756711(v=vs.85)">AUXCAPS</a> structure.


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
</table>
 




## -remarks



The device identifier in <i>uDeviceID</i> varies from zero to one less than the number of devices present. AUX_MAPPER may also be used. Use the <a href="https://docs.microsoft.com/previous-versions/dd756713(v=vs.85)">auxGetNumDevs</a> function to determine the number of auxiliary output devices present in the system.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/waveform-audio">Waveform Audio</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/waveform-functions">Waveform Functions</a>
 

 

