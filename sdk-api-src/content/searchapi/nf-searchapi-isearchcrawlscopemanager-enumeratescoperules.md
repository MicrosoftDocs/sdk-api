---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ISearchCrawlScopeManager::EnumerateScopeRules


## -description



          Returns an enumeration of all the scope rules of which this instance of the <a href="https://msdn.microsoft.com/8b731941-f1f6-402e-8cee-3c493e3c369d">ISearchCrawlScopeManager</a> interface is aware.
        


## -parameters




### -param ppSearchScopeRules [out]

Type: <b><a href="https://msdn.microsoft.com/9e285532-8f03-4572-b908-a67abd842268">IEnumSearchScopeRules</a>**</b>


          Returns a pointer to an <a href="https://msdn.microsoft.com/9e285532-8f03-4572-b908-a67abd842268">IEnumSearchScopeRules</a> interface.
        


## -returns



Type: <b>HRESULT</b>


          Returns S_OK if successful, S_FALSE if there are no rules to enumerate, or an error value otherwise. 
        




## -remarks



<b>Windows 7 and later</b>: the CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.



