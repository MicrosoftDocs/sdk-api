---
UID: NF:searchapi.IUrlAccessor.GetSize
title: IUrlAccessor::GetSize (searchapi.h)
description: Gets the size of the content designated by the URL.
helpviewer_keywords: ["GetSize","GetSize method [search]","GetSize method [search]","IUrlAccessor interface","IUrlAccessor interface [search]","GetSize method","IUrlAccessor.GetSize","IUrlAccessor::GetSize","_search_IUrlAccessor_GetSize","search._search_IUrlAccessor_GetSize","searchapi/IUrlAccessor::GetSize"]
old-location: search\_search_IUrlAccessor_GetSize.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\iurlaccessor\getsize.htm
ms.date: 12/05/2018
ms.keywords: GetSize, GetSize method [search], GetSize method [search],IUrlAccessor interface, IUrlAccessor interface [search],GetSize method, IUrlAccessor.GetSize, IUrlAccessor::GetSize, _search_IUrlAccessor_GetSize, search._search_IUrlAccessor_GetSize, searchapi/IUrlAccessor::GetSize
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
 - IUrlAccessor::GetSize
 - searchapi/IUrlAccessor::GetSize
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
 - IUrlAccessor.GetSize
---

# IUrlAccessor::GetSize


## -description

Gets the size of the content designated by the URL.

## -parameters

### -param pllSize [out]

Type: <b>ULONGLONG*</b>

Receives a pointer to the 
     number of bytes of data contained in the URL.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The value calculated in this method is a factor in determining limitations on <a href="/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a> output size. This method should return 0 for containers if the protocol implementation is for a hierarchical content source.
            

Implement this method for non-files by returning the size of the document to be indexed. For example, to index a database where each row is a document, return the best estimate of the size of the row.