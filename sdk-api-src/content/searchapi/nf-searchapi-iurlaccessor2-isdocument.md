---
UID: NF:searchapi.IUrlAccessor2.IsDocument
title: IUrlAccessor2::IsDocument (searchapi.h)
description: Ascertains whether an item URL is a document or directory.
helpviewer_keywords: ["IUrlAccessor2 interface [search]","IsDocument method","IUrlAccessor2.IsDocument","IUrlAccessor2::IsDocument","IUrlAccessor4 interface [search]","IsDocument method","IUrlAccessor4::IsDocument","IsDocument","IsDocument method [search]","IsDocument method [search]","IUrlAccessor2 interface","IsDocument method [search]","IUrlAccessor4 interface","_search_IUrlAccessor2_IsDocument","search._search_IUrlAccessor2_IsDocument","searchapi/IUrlAccessor2::IsDocument","searchapi/IUrlAccessor4::IsDocument"]
old-location: search\_search_IUrlAccessor2_IsDocument.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\iurlaccessor2\isdocument.htm
ms.date: 12/05/2018
ms.keywords: IUrlAccessor2 interface [search],IsDocument method, IUrlAccessor2.IsDocument, IUrlAccessor2::IsDocument, IUrlAccessor4 interface [search],IsDocument method, IUrlAccessor4::IsDocument, IsDocument, IsDocument method [search], IsDocument method [search],IUrlAccessor2 interface, IsDocument method [search],IUrlAccessor4 interface, _search_IUrlAccessor2_IsDocument, search._search_IUrlAccessor2_IsDocument, searchapi/IUrlAccessor2::IsDocument, searchapi/IUrlAccessor4::IsDocument
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IUrlAccessor2::IsDocument
 - searchapi/IUrlAccessor2::IsDocument
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
 - IUrlAccessor2.IsDocument
 - IUrlAccessor4.IsDocument
---

# IUrlAccessor2::IsDocument


## -description

Ascertains whether an item URL is a document or directory.



## -returns

Type: <b>HRESULT</b>

Returns S_FALSE if the item is a directory; otherwise, it returns S_OK.

