---
UID: NF:wmcontainer.IMFASFIndexer.SetIndexByteStreams
title: IMFASFIndexer::SetIndexByteStreams (wmcontainer.h)
description: Adds byte streams to be indexed.
helpviewer_keywords: ["IMFASFIndexer interface [Media Foundation]","SetIndexByteStreams method","IMFASFIndexer.SetIndexByteStreams","IMFASFIndexer::SetIndexByteStreams","SetIndexByteStreams","SetIndexByteStreams method [Media Foundation]","SetIndexByteStreams method [Media Foundation]","IMFASFIndexer interface","f116baaa-8d9b-4ac0-9263-3bb65d67ee63","mf.imfasfindexer_setindexbytestreams","wmcontainer/IMFASFIndexer::SetIndexByteStreams"]
old-location: mf\imfasfindexer_setindexbytestreams.htm
tech.root: mf
ms.assetid: f116baaa-8d9b-4ac0-9263-3bb65d67ee63
ms.date: 12/05/2018
ms.keywords: IMFASFIndexer interface [Media Foundation],SetIndexByteStreams method, IMFASFIndexer.SetIndexByteStreams, IMFASFIndexer::SetIndexByteStreams, SetIndexByteStreams, SetIndexByteStreams method [Media Foundation], SetIndexByteStreams method [Media Foundation],IMFASFIndexer interface, f116baaa-8d9b-4ac0-9263-3bb65d67ee63, mf.imfasfindexer_setindexbytestreams, wmcontainer/IMFASFIndexer::SetIndexByteStreams
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
 - IMFASFIndexer::SetIndexByteStreams
 - wmcontainer/IMFASFIndexer::SetIndexByteStreams
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
 - IMFASFIndexer.SetIndexByteStreams
---

# IMFASFIndexer::SetIndexByteStreams


## -description

Adds byte streams to be indexed.

## -parameters

### -param ppIByteStreams [in]

An array of <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> interface pointers. To get the byte stream, call <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexerbytestream">MFCreateASFIndexerByteStream</a>.

### -param cByteStreams [in]

The number of pointers in the <i>ppIByteStreams</i> array.

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
<dt><b>MF_E_ALREADY_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The indexer object has already been initialized and it  has packets which have been indexed.

</td>
</tr>
</table>

## -remarks

For a reading scenario, only one byte stream should be used by the indexer object. For an index generating scenario, it depends how many index objects are needed to be generated.

## -see-also

<a href="/windows/desktop/medfound/asf-index-object">ASF Index Object</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer">IMFASFIndexer</a>