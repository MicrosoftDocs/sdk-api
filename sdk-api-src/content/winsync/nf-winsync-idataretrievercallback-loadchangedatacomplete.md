---
UID: NF:winsync.IDataRetrieverCallback.LoadChangeDataComplete
title: IDataRetrieverCallback::LoadChangeDataComplete (winsync.h)
description: Indicates that IAsynchronousDataRetriever::LoadChangeData has finished successfully.
helpviewer_keywords: ["IDataRetrieverCallback interface [Windows Sync]","LoadChangeDataComplete method","IDataRetrieverCallback.LoadChangeDataComplete","IDataRetrieverCallback::LoadChangeDataComplete","LoadChangeDataComplete","LoadChangeDataComplete method [Windows Sync]","LoadChangeDataComplete method [Windows Sync]","IDataRetrieverCallback interface","winsync.idataretrievercallback_loadchangedatacomplete","winsync/IDataRetrieverCallback::LoadChangeDataComplete"]
old-location: winsync\idataretrievercallback_loadchangedatacomplete.htm
tech.root: winsync
ms.assetid: b48f9a91-f211-4df4-b315-dfe8d48b3db7
ms.date: 12/05/2018
ms.keywords: IDataRetrieverCallback interface [Windows Sync],LoadChangeDataComplete method, IDataRetrieverCallback.LoadChangeDataComplete, IDataRetrieverCallback::LoadChangeDataComplete, LoadChangeDataComplete, LoadChangeDataComplete method [Windows Sync], LoadChangeDataComplete method [Windows Sync],IDataRetrieverCallback interface, winsync.idataretrievercallback_loadchangedatacomplete, winsync/IDataRetrieverCallback::LoadChangeDataComplete
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDataRetrieverCallback::LoadChangeDataComplete
 - winsync/IDataRetrieverCallback::LoadChangeDataComplete
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - IDataRetrieverCallback.LoadChangeDataComplete
---

# IDataRetrieverCallback::LoadChangeDataComplete


## -description

Indicates that <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-iasynchronousdataretriever-loadchangedata">IAsynchronousDataRetriever::LoadChangeData</a> has finished successfully.

## -parameters

### -param pUnkData [in]

An object that can be used to access the data that was loaded by <b>LoadChangeData</b>.

## -returns

The possible return codes include, but are not limited to, the values shown in the following table.

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

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-idataretrievercallback">IDataRetrieverCallback Interface</a>