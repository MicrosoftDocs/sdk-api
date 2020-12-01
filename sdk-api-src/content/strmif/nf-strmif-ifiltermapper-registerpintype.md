---
UID: NF:strmif.IFilterMapper.RegisterPinType
title: IFilterMapper::RegisterPinType (strmif.h)
description: Note  The IFilterMapper interface is deprecated. Use IFilterMapper2 instead. Registers this pin type.
helpviewer_keywords: ["IFilterMapper interface [DirectShow]","RegisterPinType method","IFilterMapper.RegisterPinType","IFilterMapper::RegisterPinType","IFilterMapperRegisterPinType","RegisterPinType","RegisterPinType method [DirectShow]","RegisterPinType method [DirectShow]","IFilterMapper interface","dshow.ifiltermapper_registerpintype","strmif/IFilterMapper::RegisterPinType"]
old-location: dshow\ifiltermapper_registerpintype.htm
tech.root: dshow
ms.assetid: 7f92745b-2b97-4cc6-9755-a580827b5bba
ms.date: 12/05/2018
ms.keywords: IFilterMapper interface [DirectShow],RegisterPinType method, IFilterMapper.RegisterPinType, IFilterMapper::RegisterPinType, IFilterMapperRegisterPinType, RegisterPinType, RegisterPinType method [DirectShow], RegisterPinType method [DirectShow],IFilterMapper interface, dshow.ifiltermapper_registerpintype, strmif/IFilterMapper::RegisterPinType
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
 - IFilterMapper::RegisterPinType
 - strmif/IFilterMapper::RegisterPinType
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
 - IFilterMapper.RegisterPinType
---

# IFilterMapper::RegisterPinType


## -description

<div class="alert"><b>Note</b>  The <b>IFilterMapper</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-ifiltermapper2">IFilterMapper2</a> instead.</div>
<div> </div>
Registers this pin type.

## -parameters

### -param clsFilter

Class identifier (CLSID) of the filter to which the pin belongs.

### -param strName

Name by which it is known.

### -param clsMajorType

Major type of the media sample supported by this pin class.

### -param clsSubType

Subtype of the media sample supported by this pin class.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

The <i>clsMajorType</i> and <i>clsSubType</i> parameters specify the media type of the pin and correspond to the <a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a> structure's <b>majortype</b> and <b>subtype</b> members, respectively.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ifiltermapper">IFilterMapper Interface</a>