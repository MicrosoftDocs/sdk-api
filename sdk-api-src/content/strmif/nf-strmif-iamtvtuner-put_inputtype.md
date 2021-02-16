---
UID: NF:strmif.IAMTVTuner.put_InputType
title: IAMTVTuner::put_InputType (strmif.h)
description: The put_InputType method sets the tuner input type (cable or antenna).
helpviewer_keywords: ["IAMTVTuner interface [DirectShow]","put_InputType method","IAMTVTuner.put_InputType","IAMTVTuner::put_InputType","IAMTVTunerput_InputType","dshow.iamtvtuner_put_inputtype","put_InputType","put_InputType method [DirectShow]","put_InputType method [DirectShow]","IAMTVTuner interface","strmif/IAMTVTuner::put_InputType"]
old-location: dshow\iamtvtuner_put_inputtype.htm
tech.root: dshow
ms.assetid: d23df6b1-eddc-4c8c-a3c9-400f915e35c4
ms.date: 12/05/2018
ms.keywords: IAMTVTuner interface [DirectShow],put_InputType method, IAMTVTuner.put_InputType, IAMTVTuner::put_InputType, IAMTVTunerput_InputType, dshow.iamtvtuner_put_inputtype, put_InputType, put_InputType method [DirectShow], put_InputType method [DirectShow],IAMTVTuner interface, strmif/IAMTVTuner::put_InputType
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
 - IAMTVTuner::put_InputType
 - strmif/IAMTVTuner::put_InputType
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
 - IAMTVTuner.put_InputType
---

# IAMTVTuner::put_InputType


## -description

The <code>put_InputType</code> method sets the tuner input type (cable or antenna).

## -parameters

### -param lIndex [in]

Index value that specifies the input pin to be set.

### -param InputType [in]

Value indicating the connection type, as specified in the [TunerInputType](/windows/desktop/api/strmif/ne-strmif-tunerinputtype) enumeration.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtvtuner">IAMTVTuner Interface</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtuner">IAMTuner Interface</a>