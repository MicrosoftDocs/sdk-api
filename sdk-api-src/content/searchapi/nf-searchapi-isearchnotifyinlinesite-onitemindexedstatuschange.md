---
UID: NF:searchapi.ISearchNotifyInlineSite.OnItemIndexedStatusChange
title: ISearchNotifyInlineSite::OnItemIndexedStatusChange
author: windows-driver-content
description: Called by the search service to notify the client when the status of a particular document or item changes.
old-location: search\_search_ISearchNotifyInlineSite_OnItemIndexedStatusChange.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\notifications\isearchnotifyinlinesite\onitemindexedstatuschange.htm
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: ISearchNotifyInlineSite interface [search],OnItemIndexedStatusChange method, ISearchNotifyInlineSite.OnItemIndexedStatusChange, ISearchNotifyInlineSite::OnItemIndexedStatusChange, OnItemIndexedStatusChange, OnItemIndexedStatusChange method [search], OnItemIndexedStatusChange method [search],ISearchNotifyInlineSite interface, _search_ISearchNotifyInlineSite_OnItemIndexedStatusChange, search._search_ISearchNotifyInlineSite_OnItemIndexedStatusChange, searchapi/ISearchNotifyInlineSite::OnItemIndexedStatusChange
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: ROWSETEVENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Searchapi.h
api_name:
-	ISearchNotifyInlineSite.OnItemIndexedStatusChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ISearchNotifyInlineSite::OnItemIndexedStatusChange


## -description



            Called by the search service to notify the client when the status of a particular document or item changes.
        


## -parameters




### -param sipStatus [in]

Type: <b><a href="https://msdn.microsoft.com/fdd80abf-7362-45ca-96da-19824eb8d650">SEARCH_INDEXING_PHASE</a></b>


                    The <a href="https://msdn.microsoft.com/fdd80abf-7362-45ca-96da-19824eb8d650">SEARCH_INDEXING_PHASE</a> status of each document in the array being sent.
                


### -param dwNumEntries [in]

Type: <b>DWORD</b>


                    The number of entries in <i>rgItemStatusEntries</i>.
                


### -param rgItemStatusEntries [in]

Type: <b><a href="https://msdn.microsoft.com/c62790bf-1c96-4566-afcc-c03810677dfb">SEARCH_ITEM_INDEXING_STATUS</a>[]</b>


                    An array of <a href="https://msdn.microsoft.com/c62790bf-1c96-4566-afcc-c03810677dfb">SEARCH_ITEM_INDEXING_STATUS</a> structures containing status update information.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5837ccf6-1156-44a5-9135-3e3b47244f9d">ISearchNotifyInlineSite</a>



<a href="https://msdn.microsoft.com/817550e2-a256-48d5-9fa6-1ea04f8b8589">Notifying the Index of Changes</a>
 

 

