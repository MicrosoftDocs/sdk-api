---
UID: NF:searchapi.ISearchManager.GetIndexerVersion
title: ISearchManager::GetIndexerVersion
author: windows-sdk-content
description: Retrieves the version of the current indexer in two chunks:\_the major version signifier and the minor version signifier.
old-location: search\_search_ISearchManager_GetIndexerVersion.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchmanager\getindexerversion.htm
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetIndexerVersion, GetIndexerVersion method [search], GetIndexerVersion method [search],ISearchManager interface, ISearchManager interface [search],GetIndexerVersion method, ISearchManager.GetIndexerVersion, ISearchManager::GetIndexerVersion, _search_ISearchManager_GetIndexerVersion, search._search_ISearchManager_GetIndexerVersion, searchapi/ISearchManager::GetIndexerVersion
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Searchadmin.idl
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
-	ISearchManager.GetIndexerVersion
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISearchManager::GetIndexerVersion


## -description


Retrieves the version of the current indexer in two chunks: the major version signifier and the minor version signifier.


## -parameters




### -param pdwMajor [out]

Type: <b>DWORD*</b>

Receives the major version signifier (the number to the left of the dot).


### -param pdwMinor [out]

Type: <b>DWORD*</b>

Receives the minor version signifier (the number to the right of the dot).


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The ReindexMatchingUrls code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates ways to specify which files to re-index and how.



