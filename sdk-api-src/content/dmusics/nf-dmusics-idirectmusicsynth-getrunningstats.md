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

# IDirectMusicSynth::GetRunningStats


## -description


The <code>GetRunningStats</code> method retrieves current information about the state of the synthesizer so that an application can tell how the synth is performing.


## -parameters




### -param pStats

Pointer to a DMUS_SYNTHSTATS structure (described in Microsoft Windows SDK documentation). The method writes the synth's statistics into this structure.


## -returns



<code>GetRunningStats</code> returns S_OK if the call was successful. Otherwise, the method returns an appropriate error code. The following table shows some of the possible return status codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the method is unable to get the stats.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Indicates a bad <i>pStats</i> pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the synthesizer has not implemented this method (so expect the worst!).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_SYNTHNOTCONFIGURED</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the synth is not open or not properly configured.

</td>
</tr>
</table>
 




## -remarks



The <code>GetRunningStats</code> method returns current information about the state of the synthesizer, including CPU loading, peak volume, and how many notes were stolen (from changing priority levels; see <a href="https://msdn.microsoft.com/library/windows/hardware/ff536542">IDirectMusicSynth::SetChannelPriority</a>). The method outputs these statistics into a DMUS_SYNTHSTATS structure.

An application can call <code>GetRunningStats</code> periodically to get the status of the synthesizer as it runs. All of the running status parameters, with the exception of <i>dwFreeMemory</i>, are refreshed every second.

An application typically accesses <code>GetRunningStats</code> indirectly by calling <b>IDirectMusicPort::GetRunningStats</b>, which is described in the Windows SDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536542">IDirectMusicSynth::SetChannelPriority</a>
 

 

