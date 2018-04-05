---
UID: NF:searchapi.ISearchPersistentItemsChangedSink.StoppedMonitoringScope
title: ISearchPersistentItemsChangedSink::StoppedMonitoringScope method
author: windows-driver-content
description: Called by a notifications provider to notify the indexer to stop monitoring changes to items within a specified hierarchical scope.
old-location: search\_search_ISearchPersistentItemsChangedSink_StoppedMonitoringScope.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\notifications\isearchpersistentitemschangedsink\stoppedmonitoringscope.htm
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: ISearchPersistentItemsChangedSink, ISearchPersistentItemsChangedSink interface [search], StoppedMonitoringScope method, ISearchPersistentItemsChangedSink::StoppedMonitoringScope, StoppedMonitoringScope method [search], StoppedMonitoringScope method [search], ISearchPersistentItemsChangedSink interface, StoppedMonitoringScope,ISearchPersistentItemsChangedSink.StoppedMonitoringScope, _search_ISearchPersistentItemsChangedSink_StoppedMonitoringScope, search._search_ISearchPersistentItemsChangedSink_StoppedMonitoringScope, searchapi/ISearchPersistentItemsChangedSink::StoppedMonitoringScope
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
req.idl: Searchnotifications.idl
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
-	ISearchPersistentItemsChangedSink.StoppedMonitoringScope
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# ISearchPersistentItemsChangedSink::StoppedMonitoringScope method


## -description



            Called by a notifications provider to notify the indexer to stop monitoring changes to items within a specified hierarchical scope.
        


## -parameters




### -param pszURL [in]

Type: <b>LPCWSTR</b>

Pointer to a null-terminated Unicode string that is the address for the scope to stop monitoring.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When the notifications provider responsible for monitoring changes in the document store goes offline, it calls <b>ISearchPersistentItemsChangedSink::StoppedMonitoringScope</b> to remove the scope from the list of notification sources.



