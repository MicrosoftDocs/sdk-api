---
UID: NF:searchapi.IUrlAccessor.BindToStream
title: IUrlAccessor::BindToStream (searchapi.h)
description: Binds the item being processed to an IStream interface [Structured Storage] data stream and retrieves a pointer to that stream.
helpviewer_keywords: ["BindToStream","BindToStream method [search]","BindToStream method [search]","IUrlAccessor interface","IUrlAccessor interface [search]","BindToStream method","IUrlAccessor.BindToStream","IUrlAccessor::BindToStream","_search_IUrlAccessor_BindToStream","search._search_IUrlAccessor_BindToStream","searchapi/IUrlAccessor::BindToStream"]
old-location: search\_search_IUrlAccessor_BindToStream.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\iurlaccessor\bindtostream.htm
ms.date: 12/05/2018
ms.keywords: BindToStream, BindToStream method [search], BindToStream method [search],IUrlAccessor interface, IUrlAccessor interface [search],BindToStream method, IUrlAccessor.BindToStream, IUrlAccessor::BindToStream, _search_IUrlAccessor_BindToStream, search._search_IUrlAccessor_BindToStream, searchapi/IUrlAccessor::BindToStream
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
 - IUrlAccessor::BindToStream
 - searchapi/IUrlAccessor::BindToStream
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
 - IUrlAccessor.BindToStream
---

# IUrlAccessor::BindToStream


## -description

Binds the item being processed to an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream interface [Structured Storage]</a> data stream and retrieves a pointer to that stream.

## -parameters

### -param ppStream [out]

Type: <b>IStream**</b>

Receives the address of a pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> that contains the item represented by the URL.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 Using the information returned by the <a href="/windows/desktop/api/searchapi/nf-searchapi-iurlaccessor-getfilename">IUrlAccessor::GetFileName</a>, <a href="/windows/desktop/api/searchapi/nf-searchapi-iurlaccessor-getclsid">IUrlAccessor::GetCLSID</a>, and <a href="/windows/desktop/api/searchapi/nf-searchapi-iurlaccessor-getdocformat">IUrlAccessor::GetDocFormat</a> methods, the appropriate content <a href="/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a> object is created and passed to this stream by the IPersistStream interface.