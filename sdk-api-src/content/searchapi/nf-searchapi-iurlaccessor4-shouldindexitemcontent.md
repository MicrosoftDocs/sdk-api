---
UID: NF:searchapi.IUrlAccessor4.ShouldIndexItemContent
title: IUrlAccessor4::ShouldIndexItemContent (searchapi.h)
description: Identifies whether the item's content should be indexed.
helpviewer_keywords: ["IUrlAccessor4 interface [search]","ShouldIndexItemContent method","IUrlAccessor4.ShouldIndexItemContent","IUrlAccessor4::ShouldIndexItemContent","ShouldIndexItemContent","ShouldIndexItemContent method [search]","ShouldIndexItemContent method [search]","IUrlAccessor4 interface","_search_IUrlAccessor4_ShouldIndexItemContent","search._search_IUrlAccessor4_ShouldIndexItemContent","searchapi/IUrlAccessor4::ShouldIndexItemContent"]
old-location: search\_search_IUrlAccessor4_ShouldIndexItemContent.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\protocolhandlers\iurlaccessor4\shouldindexitemcontent.htm
ms.date: 12/05/2018
ms.keywords: IUrlAccessor4 interface [search],ShouldIndexItemContent method, IUrlAccessor4.ShouldIndexItemContent, IUrlAccessor4::ShouldIndexItemContent, ShouldIndexItemContent, ShouldIndexItemContent method [search], ShouldIndexItemContent method [search],IUrlAccessor4 interface, _search_IUrlAccessor4_ShouldIndexItemContent, search._search_IUrlAccessor4_ShouldIndexItemContent, searchapi/IUrlAccessor4::ShouldIndexItemContent
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.redist: Windows Search (WS) 4.0
ms.custom: 19H1
f1_keywords:
 - IUrlAccessor4::ShouldIndexItemContent
 - searchapi/IUrlAccessor4::ShouldIndexItemContent
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
 - IUrlAccessor4.ShouldIndexItemContent
---

# IUrlAccessor4::ShouldIndexItemContent


## -description

Identifies whether the item's content should be indexed.

## -parameters

### -param pfIndexContent [out]

Type: <b>BOOL*</b>

A pointer to a <b>BOOL</b> value that indicates whether the item's content should be indexed.

## -returns

Type: <b>HRESULT</b>

Returns S_FALSE if the item's content should not be indexed.

