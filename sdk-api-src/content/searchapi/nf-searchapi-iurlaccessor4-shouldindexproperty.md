---
UID: NF:searchapi.IUrlAccessor4.ShouldIndexProperty
title: IUrlAccessor4::ShouldIndexProperty (searchapi.h)
description: Identifies whether a property should be indexed.
helpviewer_keywords: ["IUrlAccessor4 interface [search]","ShouldIndexProperty method","IUrlAccessor4.ShouldIndexProperty","IUrlAccessor4::ShouldIndexProperty","ShouldIndexProperty","ShouldIndexProperty method [search]","ShouldIndexProperty method [search]","IUrlAccessor4 interface","search.iurlaccessor4_shouldindexproperty","searchapi/IUrlAccessor4::ShouldIndexProperty"]
old-location: search\iurlaccessor4_shouldindexproperty.htm
tech.root: search
ms.assetid: 44F10BD2-0CE5-4462-A50B-CBD63EE3B802
ms.date: 12/05/2018
ms.keywords: IUrlAccessor4 interface [search],ShouldIndexProperty method, IUrlAccessor4.ShouldIndexProperty, IUrlAccessor4::ShouldIndexProperty, ShouldIndexProperty, ShouldIndexProperty method [search], ShouldIndexProperty method [search],IUrlAccessor4 interface, search.iurlaccessor4_shouldindexproperty, searchapi/IUrlAccessor4::ShouldIndexProperty
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
 - IUrlAccessor4::ShouldIndexProperty
 - searchapi/IUrlAccessor4::ShouldIndexProperty
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
 - IUrlAccessor4.ShouldIndexProperty
---

# IUrlAccessor4::ShouldIndexProperty


## -description

Identifies whether a property should be indexed.

## -parameters

### -param key [in]

The property to index.

### -param pfIndexProperty [out]

A pointer to a value that indicates whether a property should be indexed.

## -returns

Returns S_FALSE if the property should not be indexed.

## -see-also

<a href="/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor4">IUrlAccessor4</a>