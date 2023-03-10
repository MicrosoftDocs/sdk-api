---
UID: NF:strmif.IFilterMapper.UnregisterFilterInstance
title: IFilterMapper::UnregisterFilterInstance (strmif.h)
description: Note  The IFilterMapper interface is deprecated. Use IFilterMapper2 instead. Removes the registration of this filter instance from the registry.
helpviewer_keywords: ["IFilterMapper interface [DirectShow]","UnregisterFilterInstance method","IFilterMapper.UnregisterFilterInstance","IFilterMapper::UnregisterFilterInstance","IFilterMapperUnregisterFilterInstance","UnregisterFilterInstance","UnregisterFilterInstance method [DirectShow]","UnregisterFilterInstance method [DirectShow]","IFilterMapper interface","dshow.ifiltermapper_unregisterfilterinstance","strmif/IFilterMapper::UnregisterFilterInstance"]
old-location: dshow\ifiltermapper_unregisterfilterinstance.htm
tech.root: dshow
ms.assetid: bfeb0129-f67c-4318-8206-aa08e3b5b370
ms.date: 12/05/2018
ms.keywords: IFilterMapper interface [DirectShow],UnregisterFilterInstance method, IFilterMapper.UnregisterFilterInstance, IFilterMapper::UnregisterFilterInstance, IFilterMapperUnregisterFilterInstance, UnregisterFilterInstance, UnregisterFilterInstance method [DirectShow], UnregisterFilterInstance method [DirectShow],IFilterMapper interface, dshow.ifiltermapper_unregisterfilterinstance, strmif/IFilterMapper::UnregisterFilterInstance
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
 - IFilterMapper::UnregisterFilterInstance
 - strmif/IFilterMapper::UnregisterFilterInstance
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
 - IFilterMapper.UnregisterFilterInstance
---

# IFilterMapper::UnregisterFilterInstance


## -description

<div class="alert"><b>Note</b>  The <b>IFilterMapper</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-ifiltermapper2">IFilterMapper2</a> instead.</div>
<div> </div>
Removes the registration of this filter instance from the registry.

## -parameters

### -param MRId [in]

Media resource identifier of this instance.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ifiltermapper">IFilterMapper Interface</a>