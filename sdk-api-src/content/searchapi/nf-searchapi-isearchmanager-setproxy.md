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

# ISearchManager::SetProxy


## -description


Stores information in the indexer that determines how the indexer will work and communicate with a proxy server.


## -parameters




### -param sUseProxy [in]

Type: <b><a href="https://msdn.microsoft.com/40104593-80f1-4ac5-811c-b923b1a72435">PROXY_ACCESS</a></b>

Sets whether and how to use a proxy, using one of the values enumerated in <a href="https://msdn.microsoft.com/40104593-80f1-4ac5-811c-b923b1a72435">PROXY_ACCESS</a>.


### -param fLocalByPassProxy [in]

Type: <b>BOOL</b>

Sets whether the proxy server should be bypassed for local items and URLs.


### -param dwPortNumber [in]

Type: <b>DWORD</b>

Sets the port number that the index will use to talk to the proxy server.


### -param pszProxyName [in]

Type: <b>LPCWSTR</b>

A null-terminated Unicode string containing the name of the proxy server to use.


### -param pszByPassList






#### - pszBypassList [in]

Type: <b>LPCWSTR</b>

A null-terminated Unicode string containing a comma-delimited list of items that are considered local by the indexer and are not to be accessed through a proxy server.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The ReindexMatchingUrls code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates ways to specify which files to re-index and how.



