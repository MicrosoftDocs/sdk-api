---
UID: NF:searchapi.ISearchManager.get_ProxyName
title: ISearchManager::get_ProxyName
author: windows-sdk-content
description: Retrieves the proxy name to be used by the protocol handler.
old-location: search\_search_ISearchManager_get_ProxyName.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchmanager\get_proxyname.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ISearchManager interface [search],get_ProxyName method, ISearchManager.get_ProxyName, ISearchManager::get_ProxyName, _search_ISearchManager_get_ProxyName, get_ProxyName, get_ProxyName method [search], get_ProxyName method [search],ISearchManager interface, search._search_ISearchManager_get_ProxyName, searchapi/ISearchManager::get_ProxyName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: searchapi.h
req.include-header: 
req.redist: Windows Desktop Search (WDS) 3.0
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
tech.root: 
req.typenames: ROWSETEVENT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - ISearchManager.get_ProxyName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ISearchManager::get_ProxyName


## -description


Retrieves the proxy name to be used by the protocol handler.
        


## -parameters




### -param ppszProxyName [out, retval]

Type: <b>LPWSTR*</b>

Receives a pointer to a Unicode string that contains the proxy name.
            


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The ReindexMatchingUrls code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates ways to specify which files to re-index and how.



