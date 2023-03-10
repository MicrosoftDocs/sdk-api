---
UID: NF:mfidl.IMFMediaSourceTopologyProvider.GetMediaSourceTopology
title: IMFMediaSourceTopologyProvider::GetMediaSourceTopology (mfidl.h)
description: Returns a topology for a media source that builds an internal topology.
helpviewer_keywords: ["3889768a-27bb-422e-912b-80546b6017fb","GetMediaSourceTopology","GetMediaSourceTopology method [Media Foundation]","GetMediaSourceTopology method [Media Foundation]","IMFMediaSourceTopologyProvider interface","IMFMediaSourceTopologyProvider interface [Media Foundation]","GetMediaSourceTopology method","IMFMediaSourceTopologyProvider.GetMediaSourceTopology","IMFMediaSourceTopologyProvider::GetMediaSourceTopology","mf.imfmediasourcetopologyprovider_getmediasourcetopology","mfidl/IMFMediaSourceTopologyProvider::GetMediaSourceTopology"]
old-location: mf\imfmediasourcetopologyprovider_getmediasourcetopology.htm
tech.root: mf
ms.assetid: 3889768a-27bb-422e-912b-80546b6017fb
ms.date: 12/05/2018
ms.keywords: 3889768a-27bb-422e-912b-80546b6017fb, GetMediaSourceTopology, GetMediaSourceTopology method [Media Foundation], GetMediaSourceTopology method [Media Foundation],IMFMediaSourceTopologyProvider interface, IMFMediaSourceTopologyProvider interface [Media Foundation],GetMediaSourceTopology method, IMFMediaSourceTopologyProvider.GetMediaSourceTopology, IMFMediaSourceTopologyProvider::GetMediaSourceTopology, mf.imfmediasourcetopologyprovider_getmediasourcetopology, mfidl/IMFMediaSourceTopologyProvider::GetMediaSourceTopology
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFMediaSourceTopologyProvider::GetMediaSourceTopology
 - mfidl/IMFMediaSourceTopologyProvider::GetMediaSourceTopology
dev_langs:
 - c++
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
---

# IMFMediaSourceTopologyProvider::GetMediaSourceTopology


## -description

Returns a topology for a media source that builds an internal topology.

## -parameters

### -param pPresentationDescriptor [in]

A pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor">IMFPresentationDescriptor</a> interface of the media source's presentation descriptor. To get this pointer, either call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor">IMFMediaSource::CreatePresentationDescriptor</a> on the media source, or get the pointer from the <a href="/windows/desktop/medfound/menewpresentation">MENewPresentation</a> event.

### -param ppTopology [out]

Receives a pointer to the topology's <a href="/windows/desktop/api/mfidl/nn-mfidl-imftopology">IMFTopology</a> interface. The caller must release the interface.

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

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider">IMFMediaSourceTopologyProvider</a>



<a href="/windows/desktop/medfound/sequencer-source">Sequencer Source</a>