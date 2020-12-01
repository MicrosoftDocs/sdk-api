---
UID: NF:strmif.IAMTuner.put_Mode
title: IAMTuner::put_Mode (strmif.h)
description: The put_Mode method sets a multifunction tuner to the specified mode.
helpviewer_keywords: ["IAMTuner interface [DirectShow]","put_Mode method","IAMTuner.put_Mode","IAMTuner::put_Mode","IAMTunerput_Mode","dshow.iamtuner_put_mode","put_Mode","put_Mode method [DirectShow]","put_Mode method [DirectShow]","IAMTuner interface","strmif/IAMTuner::put_Mode"]
old-location: dshow\iamtuner_put_mode.htm
tech.root: dshow
ms.assetid: 4c0691fb-e291-43eb-9828-f58474a4334d
ms.date: 12/05/2018
ms.keywords: IAMTuner interface [DirectShow],put_Mode method, IAMTuner.put_Mode, IAMTuner::put_Mode, IAMTunerput_Mode, dshow.iamtuner_put_mode, put_Mode, put_Mode method [DirectShow], put_Mode method [DirectShow],IAMTuner interface, strmif/IAMTuner::put_Mode
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
 - IAMTuner::put_Mode
 - strmif/IAMTuner::put_Mode
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
 - IAMTuner.put_Mode
---

# IAMTuner::put_Mode


## -description

The <code>put_Mode</code> method sets a multifunction tuner to the specified mode.

## -parameters

### -param lMode [in]

Flag indicating which mode to switch to. Possible values are defined in the [AMTunerModeType](/windows/desktop/api/strmif/ne-strmif-amtunermodetype) enumeration.

You can also set the mode to digital TV if the card supports it. To do this, define AMTUNER_MODE_DTV with a value of 0x0010.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtuner">IAMTuner Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamtuner-getavailablemodes">IAMTuner::GetAvailableModes</a>