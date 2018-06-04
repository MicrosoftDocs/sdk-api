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

# IDirectMusicSynthSink::GetDesiredBufferSize


## -description


The <code>GetDesiredBufferSize</code> method retrieves the synthesizer's preferred buffer size, expressed in samples.


## -parameters




### -param pdwBufferSizeInSamples

Output pointer for the buffer size. This parameter points to a caller-allocated variable into which the method writes the desired buffer length, expressed in samples.


## -returns



<code>GetDesiredBufferSize</code> returns S_OK if the call was successful. Otherwise, the method returns an appropriate error code. The following table shows some of the possible return status codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_SYNTHNOTCONFIGURED</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the synth is not set.

</td>
</tr>
</table>
 




## -remarks



The <code>GetDesiredBufferSize</code> method returns the desired buffer size based on the current format of the synth. DirectSound buffers passed to <a href="https://msdn.microsoft.com/library/windows/hardware/ff536527">IDirectMusicSynthSink::SetDirectSound</a> might be invalid unless they are at least this size.

For more information, see the description of the <b>IDirectMusicPort</b> interface in the Microsoft Windows SDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536527">IDirectMusicSynthSink::SetDirectSound</a>
 

 

