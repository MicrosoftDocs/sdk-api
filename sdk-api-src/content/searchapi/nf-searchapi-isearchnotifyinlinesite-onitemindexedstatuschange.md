---
UID: NF:searchapi.ISearchNotifyInlineSite.OnItemIndexedStatusChange
title: ISearchNotifyInlineSite::OnItemIndexedStatusChange (searchapi.h)
author: windows-sdk-content
description: Called by the search service to notify the client when the status of a particular document or item changes.
old-location: search\_search_ISearchNotifyInlineSite_OnItemIndexedStatusChange.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\notifications\isearchnotifyinlinesite\onitemindexedstatuschange.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISearchNotifyInlineSite interface [search],OnItemIndexedStatusChange method, ISearchNotifyInlineSite.OnItemIndexedStatusChange, ISearchNotifyInlineSite::OnItemIndexedStatusChange, OnItemIndexedStatusChange, OnItemIndexedStatusChange method [search], OnItemIndexedStatusChange method [search],ISearchNotifyInlineSite interface, _search_ISearchNotifyInlineSite_OnItemIndexedStatusChange, search._search_ISearchNotifyInlineSite_OnItemIndexedStatusChange, searchapi/ISearchNotifyInlineSite::OnItemIndexedStatusChange
ms.topic: method
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
 - ISearchNotifyInlineSite.OnItemIndexedStatusChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# ISearchNotifyInlineSite::OnItemIndexedStatusChange


## -description


Called by the search service to notify the client when the status of a particular document or item changes.
        


## -parameters




### -param sipStatus [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa965701(v=VS.85).aspx">SEARCH_INDEXING_PHASE</a></b>

The <a href="https://msdn.microsoft.com/en-us/library/Aa965701(v=VS.85).aspx">SEARCH_INDEXING_PHASE</a> status of each document in the array being sent.
                


### -param dwNumEntries [in]

Type: <b>DWORD</b>

The number of entries in <i>rgItemStatusEntries</i>.
                


### -param rgItemStatusEntries [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa965372(v=VS.85).aspx">SEARCH_ITEM_INDEXING_STATUS</a>[]</b>

An array of <a href="https://msdn.microsoft.com/en-us/library/Aa965372(v=VS.85).aspx">SEARCH_ITEM_INDEXING_STATUS</a> structures containing status update information.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb231458(v=VS.85).aspx">ISearchNotifyInlineSite</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb266528(v=VS.85).aspx">Notifying the Index of Changes</a>
 

 

