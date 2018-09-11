---
UID: NN:searchapi.ISearchNotifyInlineSite
title: ISearchNotifyInlineSite
author: windows-sdk-content
description: Provides methods the Search service uses to send updates on catalog and index status to notification providers.
old-location: search\_search_ISearchNotifyInlineSite.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\notifications\isearchnotifyinlinesite\isearchnotifyinlinesite.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ISearchNotifyInlineSite, ISearchNotifyInlineSite interface [search], ISearchNotifyInlineSite interface [search],described, _search_ISearchNotifyInlineSite, search._search_ISearchNotifyInlineSite, searchapi/ISearchNotifyInlineSite
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Srchntfyinlinesite.idl
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
 - Searchapi.h
api_name:
 - ISearchNotifyInlineSite
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# ISearchNotifyInlineSite interface


## -description


Provides methods the Search service uses to send updates on catalog and index status to notification providers.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchNotifyInlineSite</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISearchNotifyInlineSite</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISearchNotifyInlineSite</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231459(v=VS.85).aspx">OnCatalogStatusChange</a>
</td>
<td align="left" width="63%">
Called by the search service to notify a client when the status of the catalog changes.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231460(v=VS.85).aspx">OnItemIndexedStatusChange</a>
</td>
<td align="left" width="63%">
Called by the search service to notify the client when the status of a particular document or item changes.
        

</td>
</tr>
</table> 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb266528(v=VS.85).aspx">Notifying the Index of Changes</a>



<a href="https://msdn.microsoft.com/en-us/library/Cc678933(v=VS.85).aspx">The Indexing Process</a>
 

 

