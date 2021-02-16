---
UID: NF:wmcontainer.IMFASFIndexer.GenerateIndexEntries
title: IMFASFIndexer::GenerateIndexEntries (wmcontainer.h)
description: Accepts an ASF packet for the file and creates index entries for them.
helpviewer_keywords: ["GenerateIndexEntries","GenerateIndexEntries method [Media Foundation]","GenerateIndexEntries method [Media Foundation]","IMFASFIndexer interface","IMFASFIndexer interface [Media Foundation]","GenerateIndexEntries method","IMFASFIndexer.GenerateIndexEntries","IMFASFIndexer::GenerateIndexEntries","febc5335-a8e8-4ae9-afb2-17f09b750477","mf.imfasfindexer_generateindexentries","wmcontainer/IMFASFIndexer::GenerateIndexEntries"]
old-location: mf\imfasfindexer_generateindexentries.htm
tech.root: mf
ms.assetid: febc5335-a8e8-4ae9-afb2-17f09b750477
ms.date: 12/05/2018
ms.keywords: GenerateIndexEntries, GenerateIndexEntries method [Media Foundation], GenerateIndexEntries method [Media Foundation],IMFASFIndexer interface, IMFASFIndexer interface [Media Foundation],GenerateIndexEntries method, IMFASFIndexer.GenerateIndexEntries, IMFASFIndexer::GenerateIndexEntries, febc5335-a8e8-4ae9-afb2-17f09b750477, mf.imfasfindexer_generateindexentries, wmcontainer/IMFASFIndexer::GenerateIndexEntries
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
 - IMFASFIndexer::GenerateIndexEntries
 - wmcontainer/IMFASFIndexer::GenerateIndexEntries
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
 - IMFASFIndexer.GenerateIndexEntries
---

# IMFASFIndexer::GenerateIndexEntries


## -description

Accepts an ASF packet for the file and creates index entries for them.

## -parameters

### -param pIASFPacketSample [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a> interface of a media sample that contains the ASF packet.

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
The argument passed in is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The indexer is not initialized.

</td>
</tr>
</table>

## -remarks

The ASF indexer creates indexes for a file internally. You can get the completed index for all data packets sent to the indexer by committing the index with <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-commitindex">IMFASFIndexer::CommitIndex</a> and then calling <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getcompletedindex">IMFASFIndexer::GetCompletedIndex</a> to write the index entries into a media buffer. To determine the size of the index so you can allocate a buffer large enough to hold the index, call <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexwritespace">IMFASFIndexer::GetIndexWriteSpace</a>.

When this method creates index entries, they are immediately available for use by <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue">IMFASFIndexer::GetSeekPositionForValue</a>.
      

The media sample specified in   <i>pIASFPacketSample</i> must hold a buffer that contains a single ASF packet. Get the sample from the  ASF multiplexer by calling the <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket">IMFASFMultiplexer::GetNextPacket</a> method. 

You cannot use this method while reading an index, only when writing an index.

## -see-also

<a href="/windows/desktop/medfound/asf-index-object">ASF Index Object</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer">IMFASFIndexer</a>