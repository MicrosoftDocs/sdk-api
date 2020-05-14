---
UID: NN:winsync.IAsynchronousDataRetriever
title: IAsynchronousDataRetriever (winsync.h)
description: Represents the mechanism by which the destination provider asynchronously retrieves item data from the source provider.helpviewer_keywords: ["IAsynchronousDataRetriever","IAsynchronousDataRetriever interface [Windows Sync]","IAsynchronousDataRetriever interface [Windows Sync]","described","winsync.iasynchronousdataretriever","winsync/IAsynchronousDataRetriever"]
old-location: winsync\iasynchronousdataretriever.htm
tech.root: winsync
ms.assetid: 38f07582-908b-430e-a886-c0fc24b807ef
ms.date: 12/05/2018
ms.keywords: IAsynchronousDataRetriever, IAsynchronousDataRetriever interface [Windows Sync], IAsynchronousDataRetriever interface [Windows Sync],described, winsync.iasynchronousdataretriever, winsync/IAsynchronousDataRetriever
f1_keywords:
- winsync/IAsynchronousDataRetriever
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
- IAsynchronousDataRetriever
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAsynchronousDataRetriever interface


## -description


Represents the mechanism by which the destination provider asynchronously retrieves item data from the source provider.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAsynchronousDataRetriever</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAsynchronousDataRetriever</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAsynchronousDataRetriever</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-iasynchronousdataretriever-getidparameters">GetIdParameters</a>
</td>
<td align="left" width="63%">
Gets the ID format schema of the provider.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-iasynchronousdataretriever-loadchangedata">LoadChangeData</a>
</td>
<td align="left" width="63%">
Retrieves item data for a change.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-iasynchronousdataretriever-registercallback">RegisterCallback</a>
</td>
<td align="left" width="63%">
Registers a callback interface that will be called by the <b>IAsynchronousDataRetriever</b> object when an asynchronous method finishes processing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-iasynchronousdataretriever-revokecallback">RevokeCallback</a>
</td>
<td align="left" width="63%">
Indicates that the <b>IAsynchronousDataRetriever</b>  object must no longer use the specified callback interface and must release any references to it.


</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
 

 

