---
UID: NN:filtereg.ILoadFilter
title: ILoadFilter (filtereg.h)
description: Defines methods and properties that are implemented by the FilterRegistration object, which provides methods for loading a filter.
helpviewer_keywords: ["ILoadFilter","ILoadFilter interface [search]","ILoadFilter interface [search]","described","filtereg/ILoadFilter","search.iloadfilter"]
old-location: search\iloadfilter.htm
tech.root: search
ms.assetid: 7ac51909-fa0e-4f97-8da0-0ab4c5de7d60
ms.date: 12/05/2018
ms.keywords: ILoadFilter, ILoadFilter interface [search], ILoadFilter interface [search],described, filtereg/ILoadFilter, search.iloadfilter
req.header: filtereg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Filtereg.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: SearchSDK.lib (for CLSID_FilterRegistration)
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ILoadFilter
 - filtereg/ILoadFilter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - filtereg.h
api_name:
 - ILoadFilter
---

# ILoadFilter interface


## -description

Defines methods and properties that are implemented by the FilterRegistration object, which provides methods for loading a filter.

## -inheritance

The <b>ILoadFilter</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ILoadFilter</b> also has these types of members:

## -remarks

A filter, also known as a filter handler, is an implementation of the <a href="/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a> interface.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/search/-search-ifilter-conceptual">Developing Filter Handlers</a>



<a href="/windows/desktop/api/filtereg/ns-filtereg-filtered_data_sources">FILTERED_DATA_SOURCES</a>



<a href="/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a>



<b>Reference</b>
