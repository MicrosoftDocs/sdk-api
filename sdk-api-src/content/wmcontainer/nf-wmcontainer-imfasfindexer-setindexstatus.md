---
UID: NF:wmcontainer.IMFASFIndexer.SetIndexStatus
title: IMFASFIndexer::SetIndexStatus (wmcontainer.h)
description: Configures the index for a stream.
helpviewer_keywords: ["IMFASFIndexer interface [Media Foundation]","SetIndexStatus method","IMFASFIndexer.SetIndexStatus","IMFASFIndexer::SetIndexStatus","SetIndexStatus","SetIndexStatus method [Media Foundation]","SetIndexStatus method [Media Foundation]","IMFASFIndexer interface","bad10893-07af-4b46-bab1-2878553813b5","mf.imfasfindexer_setindexstatus","wmcontainer/IMFASFIndexer::SetIndexStatus"]
old-location: mf\imfasfindexer_setindexstatus.htm
tech.root: mf
ms.assetid: bad10893-07af-4b46-bab1-2878553813b5
ms.date: 12/05/2018
ms.keywords: IMFASFIndexer interface [Media Foundation],SetIndexStatus method, IMFASFIndexer.SetIndexStatus, IMFASFIndexer::SetIndexStatus, SetIndexStatus, SetIndexStatus method [Media Foundation], SetIndexStatus method [Media Foundation],IMFASFIndexer interface, bad10893-07af-4b46-bab1-2878553813b5, mf.imfasfindexer_setindexstatus, wmcontainer/IMFASFIndexer::SetIndexStatus
req.header: wmcontainer.h
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
 - IMFASFIndexer::SetIndexStatus
 - wmcontainer/IMFASFIndexer::SetIndexStatus
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
 - IMFASFIndexer.SetIndexStatus
---

# IMFASFIndexer::SetIndexStatus


## -description

Configures the index for a stream.

## -parameters

### -param pbIndexDescriptor [in]

The index descriptor to set. The index descriptor is an <a href="/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_descriptor">ASF_INDEX_DESCRIPTOR</a> structure, optionally followed by index-specific data.

### -param cbIndexDescriptor [in]

The size, in bytes, of the index descriptor.

### -param fGenerateIndex [in]

A Boolean value. Set to <b>TRUE</b> to have the indexer create an index of the type specified for the stream specified in the index descriptor.

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
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
At attempt was made to change the index status in a seek-only scenario. For more information, see Remarks.

</td>
</tr>
</table>

## -remarks

You must make all calls to <b>SetIndexStatus</b> before making any calls to <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-generateindexentries">IMFASFIndexer::GenerateIndexEntries</a>.

The indexer object is configured to create temporal indexes for each stream by default. Call this method only if you want to override the default settings.

You cannot use this method in an index reading scenario.  You can only use this method when writing indexes.

## -see-also

<a href="/windows/desktop/medfound/asf-index-object">ASF Index Object</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer">IMFASFIndexer</a>