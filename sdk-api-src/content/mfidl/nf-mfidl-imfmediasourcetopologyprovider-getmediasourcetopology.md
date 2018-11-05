---
UID: NF:mfidl.IMFMediaSourceTopologyProvider.GetMediaSourceTopology
title: IMFMediaSourceTopologyProvider::GetMediaSourceTopology
author: windows-sdk-content
description: Returns a topology for a media source that builds an internal topology.
old-location: mf\imfmediasourcetopologyprovider_getmediasourcetopology.htm
tech.root: medfound
ms.assetid: 3889768a-27bb-422e-912b-80546b6017fb
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: 3889768a-27bb-422e-912b-80546b6017fb, GetMediaSourceTopology, GetMediaSourceTopology method [Media Foundation], GetMediaSourceTopology method [Media Foundation],IMFMediaSourceTopologyProvider interface, IMFMediaSourceTopologyProvider interface [Media Foundation],GetMediaSourceTopology method, IMFMediaSourceTopologyProvider.GetMediaSourceTopology, IMFMediaSourceTopologyProvider::GetMediaSourceTopology, mf.imfmediasourcetopologyprovider_getmediasourcetopology, mfidl/IMFMediaSourceTopologyProvider::GetMediaSourceTopology
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFMediaSourceTopologyProvider.GetMediaSourceTopology
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaSourceTopologyProvider::GetMediaSourceTopology


## -description



Returns a topology for a media source that builds an internal topology.




## -parameters




### -param pPresentationDescriptor [in]

A pointer to the <a href="https://msdn.microsoft.com/db03e212-7021-433e-84dc-410b2cf7af87">IMFPresentationDescriptor</a> interface of the media source's presentation descriptor. To get this pointer, either call <a href="https://msdn.microsoft.com/b6ac50b7-3ef1-43cf-8126-d9a003ebd825">IMFMediaSource::CreatePresentationDescriptor</a> on the media source, or get the pointer from the <a href="https://msdn.microsoft.com/c669b2c9-5ece-4045-b691-8a71bbf491e1">MENewPresentation</a> event.


### -param ppTopology [out]

Receives a pointer to the topology's <a href="https://msdn.microsoft.com/f293e9ee-9bd2-4b3e-a4ff-53457ee910f6">IMFTopology</a> interface. The caller must release the interface.


## -returns



The method returns an HRESULT. Possible values include, but are not limited to, those in the following table.

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
Invalid argument. For example, a <b>NULL</b> input parameter, or the presentation descriptor is not valid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7c08fb54-6a78-4b6d-aae7-4b3a823eb880">IMFMediaSourceTopologyProvider</a>



<a href="https://msdn.microsoft.com/788ede68-2fd7-45f6-90cb-2426c40f7d4c">Sequencer Source</a>
 

 

