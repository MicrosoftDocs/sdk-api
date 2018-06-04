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

# ISearchCrawlScopeManager::AddHierarchicalScope


## -description



            Adds a hierarchical scope to the search engine.
        


## -parameters




### -param pszURL [in]

Type: <b>LPCWSTR</b>


                    The URL of the scope to be added.
                


### -param fInclude [in]

Type: <b>BOOL</b>

<b>TRUE</b> if this is an inclusion scope, <b>FALSE</b> if this is an exclusion scope.
                


### -param fDefault [in]

Type: <b>BOOL</b>

<b>TRUE</b> if this is to be the default scope, <b>FALSE</b> if this is not a default scope.
                


### -param fOverrideChildren [in]

Type: <b>BOOL</b>

<b>TRUE</b> if this scope overrides all of the child URL rules, <b>FALSE</b> otherwise.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method overrides existing scope rules for the URL.The preferred methods for such functionality are <a href="https://msdn.microsoft.com/948549da-7179-4f8d-956e-4daf20f8c65a">ISearchCrawlScopeManager::AddDefaultScopeRule</a> and <a href="https://msdn.microsoft.com/100bf0b4-553c-4ecd-a40d-ee2948f2c4d5">ISearchCrawlScopeManager::AddUserScopeRule</a>.

URLs passed in as parameters to <b>ISearchCrawlScopeManager::AddHierarchicalScope</b> are expected to be fully URL-decoded and without URL control codes. For example, file:///c:\My Documents is fully URL-decoded, whereas file:///c:\My%20Documents is not.

<b>Windows 7 and later</b>: the CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.



