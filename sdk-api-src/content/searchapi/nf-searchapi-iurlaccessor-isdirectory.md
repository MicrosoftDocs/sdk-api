---
UID: NF:searchapi.IUrlAccessor.IsDirectory
title: IUrlAccessor::IsDirectory (searchapi.h)
description: Ascertains whether the item URL points to a directory.
helpviewer_keywords: ["IUrlAccessor interface [search]","IsDirectory method","IUrlAccessor.IsDirectory","IUrlAccessor::IsDirectory","IsDirectory","IsDirectory method [search]","IsDirectory method [search]","IUrlAccessor interface","_search_IUrlAccessor_IsDirectory","search._search_IUrlAccessor_IsDirectory","searchapi/IUrlAccessor::IsDirectory"]
old-location: search\_search_IUrlAccessor_IsDirectory.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\iurlaccessor\isdirectory.htm
ms.date: 12/05/2018
ms.keywords: IUrlAccessor interface [search],IsDirectory method, IUrlAccessor.IsDirectory, IUrlAccessor::IsDirectory, IsDirectory, IsDirectory method [search], IsDirectory method [search],IUrlAccessor interface, _search_IUrlAccessor_IsDirectory, search._search_IUrlAccessor_IsDirectory, searchapi/IUrlAccessor::IsDirectory
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
 - IUrlAccessor::IsDirectory
 - searchapi/IUrlAccessor::IsDirectory
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
 - IUrlAccessor.IsDirectory
---

# IUrlAccessor::IsDirectory


## -description

Ascertains whether the item URL points to a directory.



## -returns

Type: <b>HRESULT</b>

Returns S_OK if the URL is a directory, otherwise S_FALSE.

