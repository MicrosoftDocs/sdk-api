---
UID: NE:filter.tagIFILTER_FLAGS
title: IFILTER_FLAGS (filter.h)
description: Indicates whether the caller should use the IPropertySetStorage and IPropertyStorage interfaces to locate additional properties.
helpviewer_keywords: ["IFILTER_FLAGS","IFILTER_FLAGS enumeration [Indexing Service]","IFILTER_FLAGS_OLE_PROPERTIES","_idxs_IFILTER_FLAGS","filter/IFILTER_FLAGS","filter/IFILTER_FLAGS_OLE_PROPERTIES","indexsrv.ifilter_flags","tagIFILTER_FLAGS"]
old-location: indexsrv\ifilter_flags.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_0j03.htm
ms.date: 12/05/2018
ms.keywords: IFILTER_FLAGS, IFILTER_FLAGS enumeration [Indexing Service], IFILTER_FLAGS_OLE_PROPERTIES, _idxs_IFILTER_FLAGS, filter/IFILTER_FLAGS, filter/IFILTER_FLAGS_OLE_PROPERTIES, indexsrv.ifilter_flags, tagIFILTER_FLAGS
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
req.typenames: IFILTER_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagIFILTER_FLAGS
 - filter/tagIFILTER_FLAGS
 - IFILTER_FLAGS
 - filter/IFILTER_FLAGS
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
 - IFILTER_FLAGS
---

# IFILTER_FLAGS enumeration


## -description

> [!Note]  
> Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use [Windows Search](/windows/desktop/search/-search-3x-wds-overview) for client side search and [Microsoft Search Server Express](https://www.microsoft.com/download/details.aspx?id=18914) for server side search.

Indicates whether the caller should use the <b>IPropertySetStorage</b> and <b>IPropertyStorage</b> interfaces to locate additional properties.

## -enum-fields

### -field IFILTER_FLAGS_OLE_PROPERTIES:1

The caller should use the <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a> and <a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a> interfaces to locate additional properties. When this flag is set, properties available through COM enumerators should not be returned from <a href="/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a>.

## -remarks

The <i>pdwFlags</i> parameter in the <a href="/windows/desktop/api/filter/nf-filter-ifilter-init">IFilter::Init</a> method allows the <a href="/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a> implementation to pass information back to the caller. For Indexing Service 3.0, the only valid flag is IFILTER_FLAGS_OLE_PROPERTIES. If OLE properties should not be enumerated, then pdwFlags should be set to zero.

## -see-also

<a href="/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a>



<a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a>



<a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a>
