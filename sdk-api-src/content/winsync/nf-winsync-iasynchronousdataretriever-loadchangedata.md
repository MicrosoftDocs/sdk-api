---
UID: NF:winsync.IAsynchronousDataRetriever.LoadChangeData
title: IAsynchronousDataRetriever::LoadChangeData (winsync.h)
description: Retrieves item data for a change. (IAsynchronousDataRetriever.LoadChangeData)
helpviewer_keywords: ["IAsynchronousDataRetriever interface [Windows Sync]","LoadChangeData method","IAsynchronousDataRetriever.LoadChangeData","IAsynchronousDataRetriever::LoadChangeData","LoadChangeData","LoadChangeData method [Windows Sync]","LoadChangeData method [Windows Sync]","IAsynchronousDataRetriever interface","winsync.iasynchronousdataretriever_loadchangedata","winsync/IAsynchronousDataRetriever::LoadChangeData"]
old-location: winsync\iasynchronousdataretriever_loadchangedata.htm
tech.root: winsync
ms.assetid: b5e73504-1f9e-4a58-9bd9-2c184372b970
ms.date: 12/05/2018
ms.keywords: IAsynchronousDataRetriever interface [Windows Sync],LoadChangeData method, IAsynchronousDataRetriever.LoadChangeData, IAsynchronousDataRetriever::LoadChangeData, LoadChangeData, LoadChangeData method [Windows Sync], LoadChangeData method [Windows Sync],IAsynchronousDataRetriever interface, winsync.iasynchronousdataretriever_loadchangedata, winsync/IAsynchronousDataRetriever::LoadChangeData
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
 - IAsynchronousDataRetriever::LoadChangeData
 - winsync/IAsynchronousDataRetriever::LoadChangeData
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
 - IAsynchronousDataRetriever.LoadChangeData
---

# IAsynchronousDataRetriever::LoadChangeData


## -description

Retrieves item data for a change.

## -parameters

### -param pLoadChangeContext [in]

Metadata that describes the change for which data should be retrieved.

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
<tr>
<td width="40%">
<dl>
<dt><b>Provider-determined error codes.</b></dt>
</dl>
</td>
<td width="60%">
See Remarks.

</td>
</tr>
</table>

## -remarks

When <b>LoadChangeData</b> is called, the provider must take one of the following actions:

<ul>
<li>Return a success code from the method and later call <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-idataretrievercallback-loadchangedatacomplete">IDataRetrieverCallback::LoadChangeDataComplete</a> to report that asynchronous processing finished successfully.</li>
<li>Return a success code from the method and later call <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-idataretrievercallback-loadchangedataerror">IDataRetrieverCallback::LoadChangeDataError</a> to report that an error occurred during asynchronous processing.</li>
<li>Return an error code from the method. In this case, <a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-idataretrievercallback">IDataRetrieverCallback</a> methods should not be called.</li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-iasynchronousdataretriever">IAsynchronousDataRetriever Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-idataretrievercallback">IDataRetrieverCallback Interface</a>
