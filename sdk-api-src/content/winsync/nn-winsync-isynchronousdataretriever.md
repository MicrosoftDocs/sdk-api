---
UID: NN:winsync.ISynchronousDataRetriever
title: ISynchronousDataRetriever (winsync.h)
description: Represents the mechanism by which the destination provider retrieves item data from the source provider.
helpviewer_keywords: ["ISynchronousDataRetriever","ISynchronousDataRetriever interface [Windows Sync]","ISynchronousDataRetriever interface [Windows Sync]","described","winsync.isynchronousdataretriever","winsync/ISynchronousDataRetriever"]
old-location: winsync\isynchronousdataretriever.htm
tech.root: winsync
ms.assetid: d59a5198-5878-4a48-b6c4-042afc36054d
ms.date: 12/05/2018
ms.keywords: ISynchronousDataRetriever, ISynchronousDataRetriever interface [Windows Sync], ISynchronousDataRetriever interface [Windows Sync],described, winsync.isynchronousdataretriever, winsync/ISynchronousDataRetriever
f1_keywords:
- winsync/ISynchronousDataRetriever
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
- ISynchronousDataRetriever
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISynchronousDataRetriever interface


## -description


Represents the mechanism by which the destination provider retrieves item data from the source provider.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISynchronousDataRetriever</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISynchronousDataRetriever</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISynchronousDataRetriever</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isynchronousdataretriever-getidparameters">GetIdParameters</a>
</td>
<td align="left" width="63%">
Gets the ID format schema of the provider.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isynchronousdataretriever-loadchangedata">LoadChangeData</a>
</td>
<td align="left" width="63%">
Retrieves item data for a change.


</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
 

 

