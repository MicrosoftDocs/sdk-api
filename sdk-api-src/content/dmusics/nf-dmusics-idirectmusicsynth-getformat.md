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

# IDirectMusicSynth::GetFormat


## -description


The <code>GetFormat</code> method retrieves information about the wave format.


## -parameters




### -param pWaveFormatEx

Pointer to a caller-allocated <a href="https://msdn.microsoft.com/library/windows/hardware/ff538799">WAVEFORMATEX</a> structure into which the method writes information about the format. This value can be <b>NULL</b>. For more information, see the following Remarks section.


### -param pdwWaveFormatExSize

Pointer to a caller-allocated DWORD variable specifying the size in bytes of the structure that <i>pWaveFormatEx</i> points to. For more information, see the following Remarks section.


## -returns



<code>GetFormat</code> returns S_OK if the call was successful. Otherwise, the method returns an appropriate error code. The following table shows some of the possible return status codes.

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
Indicates that one of the pointers is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_SYNTHNOTCONFIGURED</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the synth is not open or is not properly configured.

</td>
</tr>
</table>
 




## -remarks



The WAVEFORMATEX structure can have a variable length that depends on the details of the format. Therefore, before retrieving the format description, an application will first query the <b>IDirectMusicSynth</b> object for the size of the format by calling this method and specifying <b>NULL</b> for the <i>pWaveFormatEx</i> parameter. In this case, the synth should return the size of the structure in the <i>pdwWaveFormatExSize</i> parameter. The application can then allocate sufficient memory and call <code>IDirectMusicSynth::GetFormat</code> again to retrieve the format description.

If the <i>pWaveFormatEx</i> parameter is not <b>NULL</b>, DirectMusic writes, at most, <i>pdwWaveFormatExSize</i> bytes to <i>pWaveFormatEx</i>.

For more information, see the description of the <b>IDirectMusicPort</b> interface and <b>IDirectMusicPort::GetFormat</b> method in the Microsoft Windows SDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538799">WAVEFORMATEX</a>
 

 

