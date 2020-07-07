---
UID: NN:winsync.IDataRetrieverCallback
title: IDataRetrieverCallback (winsync.h)
description: Represents methods that an IAsynchronousDataRetriever object can call to indicate that processing has been completed on an IAsynchronousDataRetriever method.
helpviewer_keywords: ["IDataRetrieverCallback","IDataRetrieverCallback interface [Windows Sync]","IDataRetrieverCallback interface [Windows Sync]","described","winsync.idataretrievercallback","winsync/IDataRetrieverCallback"]
old-location: winsync\idataretrievercallback.htm
tech.root: winsync
ms.assetid: fc49614d-fdd7-433a-a942-f442edf1c69f
ms.date: 12/05/2018
ms.keywords: IDataRetrieverCallback, IDataRetrieverCallback interface [Windows Sync], IDataRetrieverCallback interface [Windows Sync],described, winsync.idataretrievercallback, winsync/IDataRetrieverCallback
f1_keywords:
- winsync/IDataRetrieverCallback
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- winsync.h
api_name:
- IDataRetrieverCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDataRetrieverCallback interface


## -description


Represents methods that an <b>IAsynchronousDataRetriever</b> object can call to indicate that processing has been completed on an <b>IAsynchronousDataRetriever</b> method.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDataRetrieverCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDataRetrieverCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDataRetrieverCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-idataretrievercallback-loadchangedatacomplete">LoadChangeDataComplete</a>
</td>
<td align="left" width="63%">
Indicates that <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-iasynchronousdataretriever-loadchangedata">IAsynchronousDataRetriever::LoadChangeData</a> has finished successfully.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-idataretrievercallback-loadchangedataerror">LoadChangeDataError</a>
</td>
<td align="left" width="63%">
Indicates that an <b>IAsynchronousDataRetriever</b> method failed.



</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
 

 

