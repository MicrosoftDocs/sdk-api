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

# IMFSequencerSource::GetPresentationContext


## -description



Maps a presentation descriptor to its associated sequencer element identifier and the topology it represents.




## -parameters




### -param pPD [in]

Pointer to the <a href="https://msdn.microsoft.com/db03e212-7021-433e-84dc-410b2cf7af87">IMFPresentationDescriptor</a> interface of the presentation descriptor.


### -param pId [out]

Receives the sequencer element identifier. This value is assigned by the sequencer source when the application calls <a href="https://msdn.microsoft.com/4ff20d56-6095-495d-89ee-9086c61da8ac">IMFSequencerSource::AppendTopology</a>. This parameter is optional and can be <b>NULL</b>.


### -param ppTopology [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/f293e9ee-9bd2-4b3e-a4ff-53457ee910f6">IMFTopology</a> interface of the original topology that the application added to the sequencer source. The caller must release the interface. This parameter can receive the value <b>NULL</b> if the sequencer source has switched to the next presentation. This parameter is optional and can be <b>NULL</b>.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The presentation descriptor is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_S_SEQUENCER_CONTEXT_CANCELED</b></dt>
</dl>
</td>
<td width="60%">
This segment was canceled.

</td>
</tr>
</table>
 




## -remarks



The topology returned in <i>ppTopology</i> is the original topology that the application specified in <a href="https://msdn.microsoft.com/4ff20d56-6095-495d-89ee-9086c61da8ac">AppendTopology</a>. The source nodes in this topology contain pointers to the native sources. Do not queue this topology on the Media Session. Instead, call <a href="https://msdn.microsoft.com/3889768a-27bb-422e-912b-80546b6017fb">IMFMediaSourceTopologyProvider::GetMediaSourceTopology</a> to get the sequencer source's modified topology. The source nodes in the modified topology contain pointers to the sequencer source, rather than the native sources.




## -see-also




<a href="https://msdn.microsoft.com/ba5e8e7b-5b0e-4807-a459-75bd5727d1e2">IMFSequencerSource</a>



<a href="https://msdn.microsoft.com/788ede68-2fd7-45f6-90cb-2426c40f7d4c">Sequencer Source</a>
 

 

