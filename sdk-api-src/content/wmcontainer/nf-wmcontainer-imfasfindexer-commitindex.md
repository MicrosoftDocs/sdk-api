---
UID: NF:wmcontainer.IMFASFIndexer.CommitIndex
title: IMFASFIndexer::CommitIndex (wmcontainer.h)
description: Adds information about a new index to the ContentInfo object associated with ASF content. You must call this method before copying the index to the content so that the index will be readable by the indexer later.
helpviewer_keywords: ["44b889e1-8860-44fa-b19f-5be9f844a194","CommitIndex","CommitIndex method [Media Foundation]","CommitIndex method [Media Foundation]","IMFASFIndexer interface","IMFASFIndexer interface [Media Foundation]","CommitIndex method","IMFASFIndexer.CommitIndex","IMFASFIndexer::CommitIndex","mf.imfasfindexer_commitindex","wmcontainer/IMFASFIndexer::CommitIndex"]
old-location: mf\imfasfindexer_commitindex.htm
tech.root: medfound
ms.assetid: 44b889e1-8860-44fa-b19f-5be9f844a194
ms.date: 12/05/2018
ms.keywords: 44b889e1-8860-44fa-b19f-5be9f844a194, CommitIndex, CommitIndex method [Media Foundation], CommitIndex method [Media Foundation],IMFASFIndexer interface, IMFASFIndexer interface [Media Foundation],CommitIndex method, IMFASFIndexer.CommitIndex, IMFASFIndexer::CommitIndex, mf.imfasfindexer_commitindex, wmcontainer/IMFASFIndexer::CommitIndex
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
 - IMFASFIndexer::CommitIndex
 - wmcontainer/IMFASFIndexer::CommitIndex
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
 - IMFASFIndexer.CommitIndex
---

# IMFASFIndexer::CommitIndex


## -description

Adds information about a new index to the ContentInfo object associated with ASF content. You must call this method before copying the index to the content so that the index will be readable by the indexer later.

## -parameters

### -param pIContentInfo [in]

Pointer to the <a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo">IMFASFContentInfo</a> interface of the ContentInfo object that describes the content.

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
The caller made an invalid request. For more information, see Remarks.

</td>
</tr>
</table>

## -remarks

For the index to function properly, you must call this method after all ASF packets in the file have been passed to the indexer by using the <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-generateindexentries">IMFASFIndexer::GenerateIndexEntries</a> method. After you call this method, you must retrieve the indexes by calling <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getcompletedindex">GetCompletedIndex</a> and write them to the appropriate location in the file. Finally, you must generate a new ASF header by calling the <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader">IMFASFContentInfo::GenerateHeader</a> method of the ASF ContentInfo object.

 An application must use the <b>CommitIndex</b> method only when writing a new index otherwise <b>CommitIndex</b> may return MF_E_INVALIDREQUEST as a result. For example, MF_E_INVALIDREQUEST is returned if the application has flags other than MFASF_INDEXER_WRITE_NEW_INDEX  set on the indexer object. <b>CommitIndex</b> can also return MFASF_INDEXER_WRITE_NEW_INDEX if the index entries have already been committed through an earlier <b>CommitIndex</b> call.

You cannot use this method in an index reading scenario.  You can only use this method when writing indexes.

## -see-also

<a href="/windows/desktop/medfound/asf-index-object">ASF Index Object</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer">IMFASFIndexer</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer">MFCreateASFIndexer</a>