---
UID: NF:mfidl.IMFSequencerSource.UpdateTopology
title: IMFSequencerSource::UpdateTopology (mfidl.h)
description: Updates a topology in the queue.
helpviewer_keywords: ["4ed6be6c-a031-4628-a3c5-7f0676cc0baf","IMFSequencerSource interface [Media Foundation]","UpdateTopology method","IMFSequencerSource.UpdateTopology","IMFSequencerSource::UpdateTopology","UpdateTopology","UpdateTopology method [Media Foundation]","UpdateTopology method [Media Foundation]","IMFSequencerSource interface","mf.imfsequencersource_updatetopology","mfidl/IMFSequencerSource::UpdateTopology"]
old-location: mf\imfsequencersource_updatetopology.htm
tech.root: mf
ms.assetid: 4ed6be6c-a031-4628-a3c5-7f0676cc0baf
ms.date: 12/05/2018
ms.keywords: 4ed6be6c-a031-4628-a3c5-7f0676cc0baf, IMFSequencerSource interface [Media Foundation],UpdateTopology method, IMFSequencerSource.UpdateTopology, IMFSequencerSource::UpdateTopology, UpdateTopology, UpdateTopology method [Media Foundation], UpdateTopology method [Media Foundation],IMFSequencerSource interface, mf.imfsequencersource_updatetopology, mfidl/IMFSequencerSource::UpdateTopology
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
 - IMFSequencerSource::UpdateTopology
 - mfidl/IMFSequencerSource::UpdateTopology
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
 - IMFSequencerSource.UpdateTopology
---

# IMFSequencerSource::UpdateTopology


## -description

Updates a topology in the queue.

## -parameters

### -param dwId [in]

Sequencer element identifier of the topology to update.

### -param pTopology [in]

Pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imftopology">IMFTopology</a> interface of the updated topology object.

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
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The sequencer source has been shut down.

</td>
</tr>
</table>

## -remarks

This method is asynchronous. When the operation is completed, the sequencer source sends an <a href="/windows/desktop/medfound/mesequencersourcetopologyupdated">MESequencerSourceTopologyUpdated</a> event.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource">IMFSequencerSource</a>



<a href="/windows/desktop/medfound/sequencer-source">Sequencer Source</a>