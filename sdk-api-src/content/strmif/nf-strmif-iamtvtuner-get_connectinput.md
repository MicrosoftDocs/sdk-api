---
UID: NF:strmif.IAMTVTuner.get_ConnectInput
title: IAMTVTuner::get_ConnectInput (strmif.h)
description: The get_ConnectInput method retrieves the hardware tuner input connection.
helpviewer_keywords: ["IAMTVTuner interface [DirectShow]","get_ConnectInput method","IAMTVTuner.get_ConnectInput","IAMTVTuner::get_ConnectInput","IAMTVTunerget_ConnectInput","dshow.iamtvtuner_get_connectinput","get_ConnectInput","get_ConnectInput method [DirectShow]","get_ConnectInput method [DirectShow]","IAMTVTuner interface","strmif/IAMTVTuner::get_ConnectInput"]
old-location: dshow\iamtvtuner_get_connectinput.htm
tech.root: dshow
ms.assetid: 9dbcdc9f-7efe-4784-a60c-a6c161befb9b
ms.date: 12/05/2018
ms.keywords: IAMTVTuner interface [DirectShow],get_ConnectInput method, IAMTVTuner.get_ConnectInput, IAMTVTuner::get_ConnectInput, IAMTVTunerget_ConnectInput, dshow.iamtvtuner_get_connectinput, get_ConnectInput, get_ConnectInput method [DirectShow], get_ConnectInput method [DirectShow],IAMTVTuner interface, strmif/IAMTVTuner::get_ConnectInput
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
 - IAMTVTuner::get_ConnectInput
 - strmif/IAMTVTuner::get_ConnectInput
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
 - IAMTVTuner.get_ConnectInput
---

# IAMTVTuner::get_ConnectInput


## -description

The <code>get_ConnectInput</code> method retrieves the hardware tuner input connection.

## -parameters

### -param plIndex [out]

Pointer to the input pin to get the connection for.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtvtuner">IAMTVTuner Interface</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtuner">IAMTuner Interface</a>