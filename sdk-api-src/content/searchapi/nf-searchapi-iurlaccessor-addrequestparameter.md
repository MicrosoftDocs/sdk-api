---
UID: NF:searchapi.IUrlAccessor.AddRequestParameter
title: IUrlAccessor::AddRequestParameter (searchapi.h)
description: Requests a property-value set.
helpviewer_keywords: ["AddRequestParameter","AddRequestParameter method [search]","AddRequestParameter method [search]","IUrlAccessor interface","IUrlAccessor interface [search]","AddRequestParameter method","IUrlAccessor.AddRequestParameter","IUrlAccessor::AddRequestParameter","_search_IUrlAccessor_AddRequestParameter","search._search_IUrlAccessor_AddRequestParameter","searchapi/IUrlAccessor::AddRequestParameter"]
old-location: search\_search_IUrlAccessor_AddRequestParameter.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\iurlaccessor\addrequestparameter.htm
ms.date: 12/05/2018
ms.keywords: AddRequestParameter, AddRequestParameter method [search], AddRequestParameter method [search],IUrlAccessor interface, IUrlAccessor interface [search],AddRequestParameter method, IUrlAccessor.AddRequestParameter, IUrlAccessor::AddRequestParameter, _search_IUrlAccessor_AddRequestParameter, search._search_IUrlAccessor_AddRequestParameter, searchapi/IUrlAccessor::AddRequestParameter
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
 - IUrlAccessor::AddRequestParameter
 - searchapi/IUrlAccessor::AddRequestParameter
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
 - IUrlAccessor.AddRequestParameter
---

# IUrlAccessor::AddRequestParameter


## -description

Requests a property-value set.

## -parameters

### -param pSpec [in]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propspec">PROPSPEC</a>*</b>

Pointer to a <a href="/windows/desktop/api/propidl/ns-propidl-propspec">PROPSPEC</a> structure containing the requested property.

### -param pVar [in]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

Pointer to a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure containing the value for the property specified by <i>pSpec</i>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Implement this method to obtain additional information from the content source (for instance, the If-Modified-Since header in an HTTP request).