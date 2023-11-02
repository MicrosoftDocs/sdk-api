---
UID: NF:searchapi.ISearchRoot.get_AuthenticationType
title: ISearchRoot::get_AuthenticationType (searchapi.h)
description: Retrieves the type of authentication needed to access the URLs under this search root.
helpviewer_keywords: ["ISearchRoot interface [search]","get_AuthenticationType method","ISearchRoot.get_AuthenticationType","ISearchRoot::get_AuthenticationType","_search_ISearchRoot_get_AuthenticationType","get_AuthenticationType","get_AuthenticationType method [search]","get_AuthenticationType method [search]","ISearchRoot interface","search._search_ISearchRoot_get_AuthenticationType","searchapi/ISearchRoot::get_AuthenticationType"]
old-location: search\_search_ISearchRoot_get_AuthenticationType.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchroot\get_authenticationtype.htm
ms.date: 12/05/2018
ms.keywords: ISearchRoot interface [search],get_AuthenticationType method, ISearchRoot.get_AuthenticationType, ISearchRoot::get_AuthenticationType, _search_ISearchRoot_get_AuthenticationType, get_AuthenticationType, get_AuthenticationType method [search], get_AuthenticationType method [search],ISearchRoot interface, search._search_ISearchRoot_get_AuthenticationType, searchapi/ISearchRoot::get_AuthenticationType
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
 - ISearchRoot::get_AuthenticationType
 - searchapi/ISearchRoot::get_AuthenticationType
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
 - ISearchRoot.get_AuthenticationType
---

# ISearchRoot::get_AuthenticationType


## -description

Retrieves the type of authentication needed to access the URLs under this search root.

## -parameters

### -param pAuthType [out, retval]

Type: <b><a href="/windows/desktop/api/searchapi/ne-searchapi-auth_type">AUTH_TYPE</a>*</b>

A pointer to a value from the <a href="/windows/desktop/api/searchapi/ne-searchapi-auth_type">AUTH_TYPE</a> enumeration that indicates the authentication type required to access URLs under this search root.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>Windows 7 and later</b>: Check out the <a href="/windows/win32/search/-search-sample-crawlscopecommandline">CrawlScopeCommandLine code sample</a> to see how to define command line 
options for Crawl Scope Manager (CSM) indexing operations.