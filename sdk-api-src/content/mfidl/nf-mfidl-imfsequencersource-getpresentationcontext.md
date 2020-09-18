---
UID: NF:mfidl.IMFSequencerSource.GetPresentationContext
title: IMFSequencerSource::GetPresentationContext (mfidl.h)
description: Maps a presentation descriptor to its associated sequencer element identifier and the topology it represents.
helpviewer_keywords: ["GetPresentationContext","GetPresentationContext method [Media Foundation]","GetPresentationContext method [Media Foundation]","IMFSequencerSource interface","IMFSequencerSource interface [Media Foundation]","GetPresentationContext method","IMFSequencerSource.GetPresentationContext","IMFSequencerSource::GetPresentationContext","c444ccad-68b8-40eb-9e87-0b4d61ac725d","mf.imfsequencersource_getpresentationcontext","mfidl/IMFSequencerSource::GetPresentationContext"]
old-location: mf\imfsequencersource_getpresentationcontext.htm
tech.root: mf
ms.assetid: c444ccad-68b8-40eb-9e87-0b4d61ac725d
ms.date: 12/05/2018
ms.keywords: GetPresentationContext, GetPresentationContext method [Media Foundation], GetPresentationContext method [Media Foundation],IMFSequencerSource interface, IMFSequencerSource interface [Media Foundation],GetPresentationContext method, IMFSequencerSource.GetPresentationContext, IMFSequencerSource::GetPresentationContext, c444ccad-68b8-40eb-9e87-0b4d61ac725d, mf.imfsequencersource_getpresentationcontext, mfidl/IMFSequencerSource::GetPresentationContext
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
 - IMFSequencerSource::GetPresentationContext
 - mfidl/IMFSequencerSource::GetPresentationContext
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
 - IMFSequencerSource.GetPresentationContext
---

# IMFSequencerSource::GetPresentationContext


## -description

Maps a presentation descriptor to its associated sequencer element identifier and the topology it represents.

## -parameters

### -param pPD [in]

Pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor">IMFPresentationDescriptor</a> interface of the presentation descriptor.

### -param pId [out]

Receives the sequencer element identifier. This value is assigned by the sequencer source when the application calls <a href="/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology">IMFSequencerSource::AppendTopology</a>. This parameter is optional and can be <b>NULL</b>.

### -param ppTopology [out]

Receives a pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imftopology">IMFTopology</a> interface of the original topology that the application added to the sequencer source. The caller must release the interface. This parameter can receive the value <b>NULL</b> if the sequencer source has switched to the next presentation. This parameter is optional and can be <b>NULL</b>.

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

The topology returned in <i>ppTopology</i> is the original topology that the application specified in <a href="/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology">AppendTopology</a>. The source nodes in this topology contain pointers to the native sources. Do not queue this topology on the Media Session. Instead, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology">IMFMediaSourceTopologyProvider::GetMediaSourceTopology</a> to get the sequencer source's modified topology. The source nodes in the modified topology contain pointers to the sequencer source, rather than the native sources.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource">IMFSequencerSource</a>



<a href="/windows/desktop/medfound/sequencer-source">Sequencer Source</a>