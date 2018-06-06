---
UID: NF:searchapi.ISearchRoot.get_AuthenticationType
title: ISearchRoot::get_AuthenticationType
author: windows-sdk-content
description: Retrieves the type of authentication needed to access the URLs under this this search root.
old-location: search\_search_ISearchRoot_get_AuthenticationType.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchroot\get_authenticationtype.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: ISearchRoot interface [search],get_AuthenticationType method, ISearchRoot.get_AuthenticationType, ISearchRoot::get_AuthenticationType, _search_ISearchRoot_get_AuthenticationType, get_AuthenticationType, get_AuthenticationType method [search], get_AuthenticationType method [search],ISearchRoot interface, search._search_ISearchRoot_get_AuthenticationType, searchapi/ISearchRoot::get_AuthenticationType
ms.prod: windows
ms.technology: windows-sdk
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
req.idl: 
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
 - ISearchRoot.get_AuthenticationType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISearchRoot::get_AuthenticationType


## -description


Retrieves the type of authentication needed to access the URLs under this this search root.


## -parameters




### -param pAuthType [out, retval]

Type: <b><a href="https://msdn.microsoft.com/430a8631-6ee9-460c-a05c-d930001e1974">AUTH_TYPE</a>*</b>

A pointer to a value from the <a href="https://msdn.microsoft.com/430a8631-6ee9-460c-a05c-d930001e1974">AUTH_TYPE</a> enumeration that indicates the authentication type required to access URLs under this search root.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line 
options for Crawl Scope Manager (CSM) indexing operations.



