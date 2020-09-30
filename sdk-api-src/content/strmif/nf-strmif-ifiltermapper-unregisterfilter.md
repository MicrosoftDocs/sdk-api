---
UID: NF:strmif.IFilterMapper.UnregisterFilter
title: IFilterMapper::UnregisterFilter (strmif.h)
description: Note  The IFilterMapper interface is deprecated. Use IFilterMapper2 instead. Removes the registration of this filter from the registry.
helpviewer_keywords: ["IFilterMapper interface [DirectShow]","UnregisterFilter method","IFilterMapper.UnregisterFilter","IFilterMapper::UnregisterFilter","IFilterMapperUnregisterFilter","UnregisterFilter","UnregisterFilter method [DirectShow]","UnregisterFilter method [DirectShow]","IFilterMapper interface","dshow.ifiltermapper_unregisterfilter","strmif/IFilterMapper::UnregisterFilter"]
old-location: dshow\ifiltermapper_unregisterfilter.htm
tech.root: dshow
ms.assetid: 9b5941d4-d0e7-4f4a-b273-e0fa4a1e1c2e
ms.date: 12/05/2018
ms.keywords: IFilterMapper interface [DirectShow],UnregisterFilter method, IFilterMapper.UnregisterFilter, IFilterMapper::UnregisterFilter, IFilterMapperUnregisterFilter, UnregisterFilter, UnregisterFilter method [DirectShow], UnregisterFilter method [DirectShow],IFilterMapper interface, dshow.ifiltermapper_unregisterfilter, strmif/IFilterMapper::UnregisterFilter
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFilterMapper::UnregisterFilter
 - strmif/IFilterMapper::UnregisterFilter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IFilterMapper.UnregisterFilter
---

# IFilterMapper::UnregisterFilter


## -description

<div class="alert"><b>Note</b>  The <b>IFilterMapper</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-ifiltermapper2">IFilterMapper2</a> instead.</div>
<div> </div>
Removes the registration of this filter from the registry.

## -parameters

### -param Filter [in]

GUID of the filter.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ifiltermapper">IFilterMapper Interface</a>