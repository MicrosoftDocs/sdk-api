---
UID: NF:wmcontainer.IMFASFIndexer.GetIndexStatus
title: IMFASFIndexer::GetIndexStatus (wmcontainer.h)
description: Retrieves the index settings for a specified stream and index type.
helpviewer_keywords: ["GetIndexStatus","GetIndexStatus method [Media Foundation]","GetIndexStatus method [Media Foundation]","IMFASFIndexer interface","IMFASFIndexer interface [Media Foundation]","GetIndexStatus method","IMFASFIndexer.GetIndexStatus","IMFASFIndexer::GetIndexStatus","dc38a060-36e4-458e-829e-2770387fc484","mf.imfasfindexer_getindexstatus","wmcontainer/IMFASFIndexer::GetIndexStatus"]
old-location: mf\imfasfindexer_getindexstatus.htm
tech.root: mf
ms.assetid: dc38a060-36e4-458e-829e-2770387fc484
ms.date: 12/05/2018
ms.keywords: GetIndexStatus, GetIndexStatus method [Media Foundation], GetIndexStatus method [Media Foundation],IMFASFIndexer interface, IMFASFIndexer interface [Media Foundation],GetIndexStatus method, IMFASFIndexer.GetIndexStatus, IMFASFIndexer::GetIndexStatus, dc38a060-36e4-458e-829e-2770387fc484, mf.imfasfindexer_getindexstatus, wmcontainer/IMFASFIndexer::GetIndexStatus
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
 - IMFASFIndexer::GetIndexStatus
 - wmcontainer/IMFASFIndexer::GetIndexStatus
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
 - IMFASFIndexer.GetIndexStatus
---

# IMFASFIndexer::GetIndexStatus


## -description

Retrieves the index settings for a specified stream and index type.

## -parameters

### -param pIndexIdentifier [in]

Pointer to an <a href="/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier">ASF_INDEX_IDENTIFIER</a> structure that contains the stream number and index type for which to get the status.

### -param pfIsIndexed [out]

A variable that retrieves a Boolean value specifying whether the index described by <i>pIndexIdentifier</i> has been created.

### -param pbIndexDescriptor [out]

A buffer that receives the index descriptor. The index descriptor consists of an <a href="/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_descriptor">ASF_INDEX_DESCRIPTOR</a> structure, optionally followed by index-specific data.

### -param pcbIndexDescriptor [in, out]

On input, specifies the size, in bytes, of the buffer that <i>pbIndexDescriptor</i> points to. The value can be zero if <i>pbIndexDescriptor</i> is <b>NULL</b>. On output, receives the size of the index descriptor, in bytes.

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
<dt><b>MF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The buffer size specified in <i>pcbIndexDescriptor</i> is too small.

</td>
</tr>
</table>

## -remarks

To read an existing ASF index, call <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexbytestreams">IMFASFIndexer::SetIndexByteStreams</a> before calling this method.

If an index exists for the stream and the value passed into <i>pcbIndexDescriptor</i> is smaller than the required size of the <i>pbIndexDescriptor</i> buffer, the method returns MF_E_BUFFERTOOSMALL. The required buffer size is returned in the <i>pcbIndexDescriptor</i> parameter.

If there is no index for the specified stream, the method returns <b>FALSE</b> in the <i>pfIsIndexed</i> parameter.

## -see-also

<a href="/windows/desktop/medfound/asf-index-object">ASF Index Object</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer">IMFASFIndexer</a>