---
UID: NF:mfidl.IMFSequencerSource.UpdateTopologyFlags
title: IMFSequencerSource::UpdateTopologyFlags (mfidl.h)
description: Updates the flags for a topology in the queue.
helpviewer_keywords: ["IMFSequencerSource interface [Media Foundation]","UpdateTopologyFlags method","IMFSequencerSource.UpdateTopologyFlags","IMFSequencerSource::UpdateTopologyFlags","UpdateTopologyFlags","UpdateTopologyFlags method [Media Foundation]","UpdateTopologyFlags method [Media Foundation]","IMFSequencerSource interface","ee71b574-0456-4091-bbb0-da5c57a7506e","mf.imfsequencersource_updatetopologyflags","mfidl/IMFSequencerSource::UpdateTopologyFlags"]
old-location: mf\imfsequencersource_updatetopologyflags.htm
tech.root: mf
ms.assetid: ee71b574-0456-4091-bbb0-da5c57a7506e
ms.date: 12/05/2018
ms.keywords: IMFSequencerSource interface [Media Foundation],UpdateTopologyFlags method, IMFSequencerSource.UpdateTopologyFlags, IMFSequencerSource::UpdateTopologyFlags, UpdateTopologyFlags, UpdateTopologyFlags method [Media Foundation], UpdateTopologyFlags method [Media Foundation],IMFSequencerSource interface, ee71b574-0456-4091-bbb0-da5c57a7506e, mf.imfsequencersource_updatetopologyflags, mfidl/IMFSequencerSource::UpdateTopologyFlags
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
 - IMFSequencerSource::UpdateTopologyFlags
 - mfidl/IMFSequencerSource::UpdateTopologyFlags
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
 - IMFSequencerSource.UpdateTopologyFlags
---

# IMFSequencerSource::UpdateTopologyFlags


## -description

Updates the flags for a topology in the queue.

## -parameters

### -param dwId [in]

Sequencer element identifier of the topology to update.

### -param dwFlags [in]

Bitwise <b>OR</b> of flags from the <a href="/windows/desktop/api/mfidl/ne-mfidl-mfsequencertopologyflags">MFSequencerTopologyFlags</a> enumeration.

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
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource">IMFSequencerSource</a>



<a href="/windows/desktop/medfound/sequencer-source">Sequencer Source</a>