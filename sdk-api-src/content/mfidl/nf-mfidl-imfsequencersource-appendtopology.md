---
UID: NF:mfidl.IMFSequencerSource.AppendTopology
title: IMFSequencerSource::AppendTopology
author: windows-sdk-content
description: Adds a topology to the end of the queue.
old-location: mf\imfsequencersource_appendtopology.htm
old-project: medfound
ms.assetid: 4ff20d56-6095-495d-89ee-9086c61da8ac
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: 4ff20d56-6095-495d-89ee-9086c61da8ac, AppendTopology, AppendTopology method [Media Foundation], AppendTopology method [Media Foundation],IMFSequencerSource interface, IMFSequencerSource interface [Media Foundation],AppendTopology method, IMFSequencerSource.AppendTopology, IMFSequencerSource::AppendTopology, mf.imfsequencersource_appendtopology, mfidl/IMFSequencerSource::AppendTopology
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFSequencerSource.AppendTopology
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSequencerSource::AppendTopology


## -description



Adds a topology to the end of the queue.




## -parameters




### -param pTopology [in]

Pointer to the <a href="https://msdn.microsoft.com/f293e9ee-9bd2-4b3e-a4ff-53457ee910f6">IMFTopology</a> interface of the topology. This pointer cannot be <b>NULL</b>. If an application passes <b>NULL</b>, the call fails with an E_INVALIDARG error code.


### -param dwFlags [in]

A combination of flags from the <a href="https://msdn.microsoft.com/d52bac8c-e490-417c-ac00-e4cf57fd151c">MFSequencerTopologyFlags</a> enumeration.


### -param pdwId [out]

Receives the sequencer element identifier for this topology.


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
<dt><b>MF_E_ATTRIBUTENOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The source topology node is missing one of the following attributes:

<ul>
<li>

<a href="https://msdn.microsoft.com/5acafbc1-823f-4b6d-8737-04b3a6a0cf87">MF_TOPONODE_STREAM_DESCRIPTOR</a>


</li>
<li>

<a href="https://msdn.microsoft.com/4f2c1ad8-fda9-482f-b82a-9838d15d2785">MF_TOPONODE_PRESENTATION_DESCRIPTOR</a>


</li>
<li>

<a href="https://msdn.microsoft.com/73b84ab6-bdc2-4b22-9ce4-b79b954476e5">MF_TOPONODE_SOURCE</a>


</li>
</ul>
</td>
</tr>
</table>
 




## -remarks



The sequencer plays topologies in the order they are queued. You can queue as many topologies as you want to preroll.

The application must indicate to the sequencer when it has queued the last topology on the Media Session. To specify the last topology, set the SequencerTopologyFlags_Last flag in the <i>dwFlags</i> parameter when you append the topology. The sequencer uses this information to end playback with the pipeline. Otherwise, the sequencer waits indefinitely for a new topology to be queued.




## -see-also




<a href="https://msdn.microsoft.com/0d7ce9ca-9f34-4842-bd49-9211ae4454de">About the Sequencer Source</a>



<a href="https://msdn.microsoft.com/ba5e8e7b-5b0e-4807-a459-75bd5727d1e2">IMFSequencerSource</a>



<a href="https://msdn.microsoft.com/67c32232-09cb-4098-b80b-4b93ee121190">MFCreateTopologyNode</a>
 

 

