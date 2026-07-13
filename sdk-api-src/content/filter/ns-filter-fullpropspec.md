---
UID: NS:filter.tagFULLPROPSPEC
title: FULLPROPSPEC (filter.h)
description: Specifies a property set and a property within the property set.
helpviewer_keywords: ["FULLPROPSPEC","FULLPROPSPEC structure [Indexing Service]","_idxs_FULLPROPSPEC","filter/FULLPROPSPEC","indexsrv.fullpropspec","tagFULLPROPSPEC"]
old-location: indexsrv\fullpropspec.htm
tech.root: search
ms.assetid: VS|indexsrv|~\html\ixrefint_599f.htm
ms.date: 12/05/2018
ms.keywords: FULLPROPSPEC, FULLPROPSPEC structure [Indexing Service], _idxs_FULLPROPSPEC, filter/FULLPROPSPEC, indexsrv.fullpropspec, tagFULLPROPSPEC
req.header: filter.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FULLPROPSPEC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagFULLPROPSPEC
 - filter/tagFULLPROPSPEC
 - FULLPROPSPEC
 - filter/FULLPROPSPEC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Filter.h
api_name:
 - FULLPROPSPEC
---

# FULLPROPSPEC structure


## -description

Specifies a property set and a property within the property set.

## -struct-fields

### -field guidPropSet

The globally unique identifier (GUID) that identifies the property set.

### -field psProperty

A pointer to the <a href="/windows/desktop/api/propidl/ns-propidl-propspec">PROPSPEC</a> structure that specifies a property either by its property identifier (propid) or by the associated string name (<b>lpwstr</b>).

## -see-also

<a href="/windows/desktop/api/filter/nf-filter-ifilter-init">IFilter::Init</a>