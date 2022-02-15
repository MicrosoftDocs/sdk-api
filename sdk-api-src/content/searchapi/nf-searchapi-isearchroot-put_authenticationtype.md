---
UID: NF:searchapi.ISearchRoot.put_AuthenticationType
title: ISearchRoot::put_AuthenticationType (searchapi.h)
description: Sets the type of authentication required to access the URLs under this search root.
helpviewer_keywords: ["ISearchRoot interface [search]","put_AuthenticationType method","ISearchRoot.put_AuthenticationType","ISearchRoot::put_AuthenticationType","_search_ISearchRoot_put_AuthenticationType","put_AuthenticationType","put_AuthenticationType method [search]","put_AuthenticationType method [search]","ISearchRoot interface","search._search_ISearchRoot_put_AuthenticationType","searchapi/ISearchRoot::put_AuthenticationType"]
old-location: search\_search_ISearchRoot_put_AuthenticationType.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchroot\put_authenticationtype.htm
ms.date: 12/05/2018
ms.keywords: ISearchRoot interface [search],put_AuthenticationType method, ISearchRoot.put_AuthenticationType, ISearchRoot::put_AuthenticationType, _search_ISearchRoot_put_AuthenticationType, put_AuthenticationType, put_AuthenticationType method [search], put_AuthenticationType method [search],ISearchRoot interface, search._search_ISearchRoot_put_AuthenticationType, searchapi/ISearchRoot::put_AuthenticationType
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISearchRoot::put_AuthenticationType
 - searchapi/ISearchRoot::put_AuthenticationType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - ISearchRoot.put_AuthenticationType
---

# ISearchRoot::put_AuthenticationType


## -description

Sets the type of authentication required to access the URLs under this search root.

## -parameters

### -param authType [in]

Type: <b><a href="/windows/desktop/api/searchapi/ne-searchapi-auth_type">AUTH_TYPE</a></b>

A value from the <a href="/windows/desktop/api/searchapi/ne-searchapi-auth_type">AUTH_TYPE</a> enumeration that indicates the authentication type.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>Windows 7 and later</b>: Check out the <a href="/windows/win32/search/-search-sample-crawlscopecommandline">CrawlScopeCommandLine code sample</a> to see how to define command line 
options for Crawl Scope Manager (CSM) indexing operations.