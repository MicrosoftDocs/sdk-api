---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IDirectMusicSynth::GetAppend


## -description


The <code>GetAppend</code> method outputs the number of additional wave samples that the DirectMusic "port" needs to have appended to the end of a download buffer.


## -parameters




### -param pdwAppend

Output pointer for the number of samples to append. This parameter points to a caller-allocated variable into which the method writes a count specifying the number of appended samples for which memory is required. The required memory in bytes can be calculated from the wave format.


## -returns



<code>GetAppend</code> returns S_OK if the call was successful. Otherwise, the method returns an appropriate error code. The following table shows some of the possible return status codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the pointer buffer is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the method is not implemented.

</td>
</tr>
</table>
 




## -remarks



This method is called to determine how much extra storage to provide at the end of a download buffer. The method outputs a count indicating the number of additional wave samples by which the buffer should be extended.

When downloading a waveform, the synth might need to attach a little more data at the end of the waveform, depending on how the synth is implemented. The port's synthesis engine can use this extra memory to interpolate across a loop boundary.

For example, if a wave loops for 20 samples at the end, the interpolation math that calculates what to do as it loops back might require some extra data at the end so that it can interpolate properly.

Extending the download buffer by the <i>pdwAppend</i> amount allows the synth to simply add the extra samples to the end of the buffer. Otherwise, the synth would have to copy the contents of the download buffer to a larger buffer in order to have room to append the extra data.

Avoid confusing the term DirectMusic "port" with a DMus port driver. A DirectMusic port corresponds to a render or capture pin on a DirectMusic filter. For more information about DirectMusic ports, see the description of the <b>IDirectMusicPort</b> interface in the Microsoft Windows SDK documentation.



