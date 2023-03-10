---
UID: NF:searchapi.IProtocolHandlerSite.GetFilter
title: IProtocolHandlerSite::GetFilter (searchapi.h)
description: Retrieves the appropriate IFilteraccording to the supplied parameters.
helpviewer_keywords: ["GetFilter","GetFilter method [search]","GetFilter method [search]","IProtocolHandlerSite interface","IProtocolHandlerSite interface [search]","GetFilter method","IProtocolHandlerSite.GetFilter","IProtocolHandlerSite::GetFilter","_search_IProtocolHandlerSite_GetFilter","search._search_IProtocolHandlerSite_GetFilter","search._search_IProtocolHandlerSite_search_IProtocolHandlerSite_GetFilter_cpp","searchapi/IProtocolHandlerSite::GetFilter"]
old-location: search\_search_IProtocolHandlerSite_search_IProtocolHandlerSite_GetFilter_cpp.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\iprotocolhandlersite\getfilter.htm
ms.date: 12/05/2018
ms.keywords: GetFilter, GetFilter method [search], GetFilter method [search],IProtocolHandlerSite interface, IProtocolHandlerSite interface [search],GetFilter method, IProtocolHandlerSite.GetFilter, IProtocolHandlerSite::GetFilter, _search_IProtocolHandlerSite_GetFilter, search._search_IProtocolHandlerSite_GetFilter, search._search_IProtocolHandlerSite_search_IProtocolHandlerSite_GetFilter_cpp, searchapi/IProtocolHandlerSite::GetFilter
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Srchprth.idl
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
 - IProtocolHandlerSite::GetFilter
 - searchapi/IProtocolHandlerSite::GetFilter
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
 - IProtocolHandlerSite.GetFilter
---

# IProtocolHandlerSite::GetFilter


## -description

Retrieves the appropriate <a href="/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a> according to the supplied parameters.

## -parameters

### -param pclsidObj [in]

Type: <b>CLSID*</b>

Pointer to the CLSID of the document type from the registry. This is used for items with embedded documents to indicate the appropriate <a href="/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a> to use for that embedded document.

### -param pcwszContentType [in]

Type: <b>LPCWSTR</b>

Pointer to a null-terminated Unicode string that contains the type of the document. This is used to retrieve <a href="/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a><b>s</b> that are mapped according to MIME type.

### -param pcwszExtension [in]

Type: <b>LPCWSTR</b>

Pointer to a null-terminated Unicode string that contains the file name extension, without the preceding period. This is used to retrieve <a href="/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a> objects that are mapped according to the file name extension.

### -param ppFilter [out]

Type: <b>IFilter**</b>

Receives the address of a pointer to the <a href="/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a> that the protocol handler uses.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method queries the Filter Host to identify the appropriate <a href="/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a> object to use for the URL item.

The choice of filter is based on the file name extension, a CLSID that identifies the file's content type in the registry, or on the MIME content type. You need to provide only one of the three parameters to this method. If you provide multiple parameters, they are tested in the following order: <i>pcwszContentType</i>, <i>pclsidObj</i>, <i>pcwszExtension</i>. The first valid parameter is used to select the appropriate <a href="/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a>; the others are ignored.