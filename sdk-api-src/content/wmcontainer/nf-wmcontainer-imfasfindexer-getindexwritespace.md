---
UID: NF:wmcontainer.IMFASFIndexer.GetIndexWriteSpace
title: IMFASFIndexer::GetIndexWriteSpace (wmcontainer.h)
description: Retrieves the size, in bytes, of the buffer required to store the completed index.
helpviewer_keywords: ["8d62a357-e46e-4431-943f-334ae11c8b31","GetIndexWriteSpace","GetIndexWriteSpace method [Media Foundation]","GetIndexWriteSpace method [Media Foundation]","IMFASFIndexer interface","IMFASFIndexer interface [Media Foundation]","GetIndexWriteSpace method","IMFASFIndexer.GetIndexWriteSpace","IMFASFIndexer::GetIndexWriteSpace","mf.imfasfindexer_getindexwritespace","wmcontainer/IMFASFIndexer::GetIndexWriteSpace"]
old-location: mf\imfasfindexer_getindexwritespace.htm
tech.root: mf
ms.assetid: 8d62a357-e46e-4431-943f-334ae11c8b31
ms.date: 12/05/2018
ms.keywords: 8d62a357-e46e-4431-943f-334ae11c8b31, GetIndexWriteSpace, GetIndexWriteSpace method [Media Foundation], GetIndexWriteSpace method [Media Foundation],IMFASFIndexer interface, IMFASFIndexer interface [Media Foundation],GetIndexWriteSpace method, IMFASFIndexer.GetIndexWriteSpace, IMFASFIndexer::GetIndexWriteSpace, mf.imfasfindexer_getindexwritespace, wmcontainer/IMFASFIndexer::GetIndexWriteSpace
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
 - IMFASFIndexer::GetIndexWriteSpace
 - wmcontainer/IMFASFIndexer::GetIndexWriteSpace
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
 - IMFASFIndexer.GetIndexWriteSpace
---

# IMFASFIndexer::GetIndexWriteSpace


## -description

Retrieves the size, in bytes, of the buffer required to store the completed index.

## -parameters

### -param pcbIndexWriteSpace [out]

Receives the size of the index, in bytes

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
<dt><b>MF_E_INDEX_NOT_COMMITTED</b></dt>
</dl>
</td>
<td width="60%">
The index has not been committed. For more information; see Remarks.

</td>
</tr>
</table>

## -remarks

Use this method to get the size of the index and then allocate a buffer big enough to hold it. 

The index must be committed with a call to<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-commitindex">IMFASFIndexer::CommitIndex</a> before calling <b>IMFASFIndexer::GetIndexWriteSpace</b>.  If the index is not committed before <b>GetIndexWriteSpace</b> is called, then MF_E_INDEX_NOT_COMMITTED will be returned as a result. 

Call <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getcompletedindex">IMFASFIndexer::GetCompletedIndex</a> to write the completed index into a media buffer.

You cannot use this method in a reading scenario.  You can only use this method when writing indexes.

## -see-also

<a href="/windows/desktop/medfound/asf-index-object">ASF Index Object</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer">IMFASFIndexer</a>