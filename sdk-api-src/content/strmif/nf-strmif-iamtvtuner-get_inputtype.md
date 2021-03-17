---
UID: NF:strmif.IAMTVTuner.get_InputType
title: IAMTVTuner::get_InputType (strmif.h)
description: The get_InputType method retrieves the input type set in IAMTVTuner::put_InputType.
helpviewer_keywords: ["IAMTVTuner interface [DirectShow]","get_InputType method","IAMTVTuner.get_InputType","IAMTVTuner::get_InputType","IAMTVTunerget_InputType","dshow.iamtvtuner_get_inputtype","get_InputType","get_InputType method [DirectShow]","get_InputType method [DirectShow]","IAMTVTuner interface","strmif/IAMTVTuner::get_InputType"]
old-location: dshow\iamtvtuner_get_inputtype.htm
tech.root: dshow
ms.assetid: 49763cc3-be8b-4620-b99f-af787844c97c
ms.date: 12/05/2018
ms.keywords: IAMTVTuner interface [DirectShow],get_InputType method, IAMTVTuner.get_InputType, IAMTVTuner::get_InputType, IAMTVTunerget_InputType, dshow.iamtvtuner_get_inputtype, get_InputType, get_InputType method [DirectShow], get_InputType method [DirectShow],IAMTVTuner interface, strmif/IAMTVTuner::get_InputType
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMTVTuner::get_InputType
 - strmif/IAMTVTuner::get_InputType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMTVTuner.get_InputType
---

# IAMTVTuner::get_InputType


## -description

The <code>get_InputType</code> method retrieves the input type set in <a href="/windows/desktop/api/strmif/nf-strmif-iamtvtuner-put_inputtype">IAMTVTuner::put_InputType</a>.

## -parameters

### -param lIndex [in]

Index value that specifies the input pin that will be set.

### -param pInputType [out]

Pointer to a variable the receives a member of the [TunerInputType](/windows/desktop/api/strmif/ne-strmif-tunerinputtype) enumeration.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtvtuner">IAMTVTuner Interface</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtuner">IAMTuner Interface</a>