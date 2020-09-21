---
UID: NF:wmcontainer.IMFASFIndexer.GetIndexByteStreamCount
title: IMFASFIndexer::GetIndexByteStreamCount (wmcontainer.h)
description: Retrieves the number of byte streams that are in use by the indexer object.
helpviewer_keywords: ["GetIndexByteStreamCount","GetIndexByteStreamCount method [Media Foundation]","GetIndexByteStreamCount method [Media Foundation]","IMFASFIndexer interface","IMFASFIndexer interface [Media Foundation]","GetIndexByteStreamCount method","IMFASFIndexer.GetIndexByteStreamCount","IMFASFIndexer::GetIndexByteStreamCount","a433af8a-9e8a-4234-9694-c3a5420a1710","mf.imfasfindexer_getindexbytestreamcount","wmcontainer/IMFASFIndexer::GetIndexByteStreamCount"]
old-location: mf\imfasfindexer_getindexbytestreamcount.htm
tech.root: mf
ms.assetid: a433af8a-9e8a-4234-9694-c3a5420a1710
ms.date: 12/05/2018
ms.keywords: GetIndexByteStreamCount, GetIndexByteStreamCount method [Media Foundation], GetIndexByteStreamCount method [Media Foundation],IMFASFIndexer interface, IMFASFIndexer interface [Media Foundation],GetIndexByteStreamCount method, IMFASFIndexer.GetIndexByteStreamCount, IMFASFIndexer::GetIndexByteStreamCount, a433af8a-9e8a-4234-9694-c3a5420a1710, mf.imfasfindexer_getindexbytestreamcount, wmcontainer/IMFASFIndexer::GetIndexByteStreamCount
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
 - IMFASFIndexer::GetIndexByteStreamCount
 - wmcontainer/IMFASFIndexer::GetIndexByteStreamCount
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
 - IMFASFIndexer.GetIndexByteStreamCount
---

# IMFASFIndexer::GetIndexByteStreamCount


## -description

Retrieves the number of byte streams that are  in use by the  indexer object.

## -parameters

### -param pcByteStreams [out]

Receives the number of byte streams that are  in use by the indexer object.

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
<i>pcByteStreams</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/asf-index-object">ASF Index Object</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer">IMFASFIndexer</a>