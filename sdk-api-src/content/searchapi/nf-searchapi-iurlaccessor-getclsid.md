---
UID: NF:searchapi.IUrlAccessor.GetCLSID
title: IUrlAccessor::GetCLSID (searchapi.h)
description: Gets the CLSID for the document type of the URL item being processed.
helpviewer_keywords: ["GetCLSID","GetCLSID method [search]","GetCLSID method [search]","IUrlAccessor interface","IUrlAccessor interface [search]","GetCLSID method","IUrlAccessor.GetCLSID","IUrlAccessor::GetCLSID","_search_IUrlAccessor_GetCLSID","search._search_IUrlAccessor_GetCLSID","searchapi/IUrlAccessor::GetCLSID"]
old-location: search\_search_IUrlAccessor_GetCLSID.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\iurlaccessor\getclsid.htm
ms.date: 12/05/2018
ms.keywords: GetCLSID, GetCLSID method [search], GetCLSID method [search],IUrlAccessor interface, IUrlAccessor interface [search],GetCLSID method, IUrlAccessor.GetCLSID, IUrlAccessor::GetCLSID, _search_IUrlAccessor_GetCLSID, search._search_IUrlAccessor_GetCLSID, searchapi/IUrlAccessor::GetCLSID
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
 - IUrlAccessor::GetCLSID
 - searchapi/IUrlAccessor::GetCLSID
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
 - IUrlAccessor.GetCLSID
---

# IUrlAccessor::GetCLSID


## -description

Gets the <a href="/windows/desktop/com/clsid">CLSID</a> for the document type of the URL item being processed.

## -parameters

### -param pClsid [out]

Type: <b>CLSID*</b>

Receives a pointer to the <a href="/windows/desktop/com/clsid">CLSID</a> for the document type of the URL item being processed.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If this information is not available, you can return E_NOTIMPL or E_FAIL.