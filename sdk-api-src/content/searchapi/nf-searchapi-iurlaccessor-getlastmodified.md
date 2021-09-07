---
UID: NF:searchapi.IUrlAccessor.GetLastModified
title: IUrlAccessor::GetLastModified (searchapi.h)
description: Gets the time stamp identifying when the URL was last modified.
helpviewer_keywords: ["GetLastModified","GetLastModified method [search]","GetLastModified method [search]","IUrlAccessor interface","IUrlAccessor interface [search]","GetLastModified method","IUrlAccessor.GetLastModified","IUrlAccessor::GetLastModified","_search_IUrlAccessor_GetLastModified","search._search_IUrlAccessor_GetLastModified","searchapi/IUrlAccessor::GetLastModified"]
old-location: search\_search_IUrlAccessor_GetLastModified.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\iurlaccessor\getlastmodified.htm
ms.date: 12/05/2018
ms.keywords: GetLastModified, GetLastModified method [search], GetLastModified method [search],IUrlAccessor interface, IUrlAccessor interface [search],GetLastModified method, IUrlAccessor.GetLastModified, IUrlAccessor::GetLastModified, _search_IUrlAccessor_GetLastModified, search._search_IUrlAccessor_GetLastModified, searchapi/IUrlAccessor::GetLastModified
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Urlaccsdk.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - IUrlAccessor::GetLastModified
 - searchapi/IUrlAccessor::GetLastModified
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
 - IUrlAccessor.GetLastModified
---

# IUrlAccessor::GetLastModified


## -description

Gets the time stamp identifying when the URL was last modified.

## -parameters

### -param pftLastModified [out]

Type: <b><a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>*</b>

Receives a pointer to a variable of type <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> identifying the time stamp when the URL was last modified.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is used to determine whether a URL has changed since the last time it was indexed. If the last modified time has not changed, the indexer does not process the URL's content.  
            

Directory URLs are always processed regardless of the time stamp returned by this method.