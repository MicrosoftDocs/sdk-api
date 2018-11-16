---
UID: NF:searchapi.ISearchManager.get_LocalBypass
title: ISearchManager::get_LocalBypass
author: windows-sdk-content
description: Retrieves a value that determines whether the proxy server should be bypassed to find the item or URL.
old-location: search\_search_ISearchManager_get_LocalBypass.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchmanager\get_localbypass.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ISearchManager interface [search],get_LocalBypass method, ISearchManager.get_LocalBypass, ISearchManager::get_LocalBypass, _search_ISearchManager_get_LocalBypass, get_LocalBypass, get_LocalBypass method [search], get_LocalBypass method [search],ISearchManager interface, search._search_ISearchManager_get_LocalBypass, searchapi/ISearchManager::get_LocalBypass
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ISearchManager.get_LocalBypass
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
- apiref
: 
- COM
: 
- searchapi.h
: 
- ISearchManager.get_LocalBypass
: 
---

# ISearchManager::get_LocalBypass


## -description


Retrieves a value that determines whether the proxy server should be bypassed to find the item or URL.
        


## -parameters




### -param pfLocalBypass [out, retval]

Type: <b>BOOL*</b>

Receives a pointer to a <b>BOOL</b> value that indicates whether to bypass the proxy server to find an item or URL. <b>TRUE</b> to bypass the proxy (for local items); otherwise, <b>FALSE</b>.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Proxy servers are used as a gateway between the local area network (LAN) and the Internet, primarily for security. A proxy server accepts requests for information (on other networks or the Internet) from internal systems such as servers or work stations. The proxy server then forwards the request to the Internet resource, which keeps the address of the requesting system anonymous. When the information returns from the Internet resource, the proxy server routes the information back to the requesting system. For content on the LAN, it is not necessary to go through the proxy server to access your content; this potentially saves time and extra steps.

The value retrieved by this method helps the indexer identify how to work with content that is on a local domain or network. For nonlocal content, going through the proxy server may be appropriate, if not necessary.

The setting to bypass the proxy for local domains is stored in the indexer and is set by calling the <a href="https://msdn.microsoft.com/en-us/library/Bb231488(v=VS.85).aspx">ISearchManager::SetProxy</a> method.

The ReindexMatchingUrls code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates ways to specify which files to re-index and how.



