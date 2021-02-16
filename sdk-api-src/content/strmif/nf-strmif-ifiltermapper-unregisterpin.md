---
UID: NF:strmif.IFilterMapper.UnregisterPin
title: IFilterMapper::UnregisterPin (strmif.h)
description: Note  The IFilterMapper interface is deprecated. Use IFilterMapper2 instead. Removes the registration of this pin from the registry.
helpviewer_keywords: ["IFilterMapper interface [DirectShow]","UnregisterPin method","IFilterMapper.UnregisterPin","IFilterMapper::UnregisterPin","IFilterMapperUnregisterPin","UnregisterPin","UnregisterPin method [DirectShow]","UnregisterPin method [DirectShow]","IFilterMapper interface","dshow.ifiltermapper_unregisterpin","strmif/IFilterMapper::UnregisterPin"]
old-location: dshow\ifiltermapper_unregisterpin.htm
tech.root: dshow
ms.assetid: f8964890-53d7-4731-91b2-156e61809774
ms.date: 12/05/2018
ms.keywords: IFilterMapper interface [DirectShow],UnregisterPin method, IFilterMapper.UnregisterPin, IFilterMapper::UnregisterPin, IFilterMapperUnregisterPin, UnregisterPin, UnregisterPin method [DirectShow], UnregisterPin method [DirectShow],IFilterMapper interface, dshow.ifiltermapper_unregisterpin, strmif/IFilterMapper::UnregisterPin
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
 - IFilterMapper::UnregisterPin
 - strmif/IFilterMapper::UnregisterPin
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
 - IFilterMapper.UnregisterPin
---

# IFilterMapper::UnregisterPin


## -description

<div class="alert"><b>Note</b>  The <b>IFilterMapper</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-ifiltermapper2">IFilterMapper2</a> instead.</div>
<div> </div>
Removes the registration of this pin from the registry.

## -parameters

### -param Filter [in]

GUID of the filter that this pin is part of.

### -param Name [in]

Name of the pin.

## -returns

Returns an <b>HRESULT</b> value.