---
UID: NF:searchapi.IUrlAccessor.GetSecurityProvider
title: IUrlAccessor::GetSecurityProvider (searchapi.h)
description: Gets the security provider for the URL.
helpviewer_keywords: ["GetSecurityProvider","GetSecurityProvider method [search]","GetSecurityProvider method [search]","IUrlAccessor interface","IUrlAccessor interface [search]","GetSecurityProvider method","IUrlAccessor.GetSecurityProvider","IUrlAccessor::GetSecurityProvider","_search_IUrlAccessor_GetSecurityProvider","search._search_IUrlAccessor_GetSecurityProvider","searchapi/IUrlAccessor::GetSecurityProvider"]
old-location: search\_search_IUrlAccessor_GetSecurityProvider.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\iurlaccessor\getsecurityprovider.htm
ms.date: 12/05/2018
ms.keywords: GetSecurityProvider, GetSecurityProvider method [search], GetSecurityProvider method [search],IUrlAccessor interface, IUrlAccessor interface [search],GetSecurityProvider method, IUrlAccessor.GetSecurityProvider, IUrlAccessor::GetSecurityProvider, _search_IUrlAccessor_GetSecurityProvider, search._search_IUrlAccessor_GetSecurityProvider, searchapi/IUrlAccessor::GetSecurityProvider
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
 - IUrlAccessor::GetSecurityProvider
 - searchapi/IUrlAccessor::GetSecurityProvider
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
 - IUrlAccessor.GetSecurityProvider
---

# IUrlAccessor::GetSecurityProvider


## -description

Gets the security provider for the URL.

## -parameters

### -param pSPClsid [out]

Type: <b>CLSID*</b>

Receives a pointer to a security provider's CLSID.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

