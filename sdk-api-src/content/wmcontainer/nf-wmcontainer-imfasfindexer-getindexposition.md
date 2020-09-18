---
UID: NF:wmcontainer.IMFASFIndexer.GetIndexPosition
title: IMFASFIndexer::GetIndexPosition (wmcontainer.h)
description: Retrieves the offset of the index object from the start of the content.
helpviewer_keywords: ["7ef0e36c-1be5-44ac-8f6a-e29805c99e78","GetIndexPosition","GetIndexPosition method [Media Foundation]","GetIndexPosition method [Media Foundation]","IMFASFIndexer interface","IMFASFIndexer interface [Media Foundation]","GetIndexPosition method","IMFASFIndexer.GetIndexPosition","IMFASFIndexer::GetIndexPosition","mf.imfasfindexer_getindexposition","wmcontainer/IMFASFIndexer::GetIndexPosition"]
old-location: mf\imfasfindexer_getindexposition.htm
tech.root: mf
ms.assetid: 7ef0e36c-1be5-44ac-8f6a-e29805c99e78
ms.date: 12/05/2018
ms.keywords: 7ef0e36c-1be5-44ac-8f6a-e29805c99e78, GetIndexPosition, GetIndexPosition method [Media Foundation], GetIndexPosition method [Media Foundation],IMFASFIndexer interface, IMFASFIndexer interface [Media Foundation],GetIndexPosition method, IMFASFIndexer.GetIndexPosition, IMFASFIndexer::GetIndexPosition, mf.imfasfindexer_getindexposition, wmcontainer/IMFASFIndexer::GetIndexPosition
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
 - IMFASFIndexer::GetIndexPosition
 - wmcontainer/IMFASFIndexer::GetIndexPosition
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
 - IMFASFIndexer.GetIndexPosition
---

# IMFASFIndexer::GetIndexPosition


## -description

Retrieves the offset of the index object from the start of the content.

## -parameters

### -param pIContentInfo [in]

Pointer to the <a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo">IMFASFContentInfo</a> interface of the ContentInfo object that describes the content.

### -param pcbIndexOffset [out]

Receives the offset of the index relative to the beginning of the content described by the ContentInfo object. This is the position relative to the beginning of the ASF file.

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
<i>pIContentInfo</i> is <b>NULL</b> or <i>pcbIndexOffset</i> is <b>NULL</b>

</td>
</tr>
</table>

## -remarks

The index continues from the offset retrieved by this method to the end of the file.

You must call <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize">IMFASFIndexer::Initialize</a> to set up the indexer before calling this method.

If the index is retrieved by using more than one call to <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getcompletedindex">IMFASFIndexer::GetCompletedIndex</a>, the position of individual index portions is equal to the index offset plus the offset of the portion within the index.

## -see-also

<a href="/windows/desktop/medfound/asf-index-object">ASF Index Object</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer">IMFASFIndexer</a>