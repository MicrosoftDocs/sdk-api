---
UID: NF:vidcap.IVideoProcAmp.get_DigitalMultiplier
title: IVideoProcAmp::get_DigitalMultiplier (vidcap.h)
description: The get_DigitalMultiplier method returns the camera's digital zoom level.
helpviewer_keywords: ["IVideoProcAmp interface [DirectShow]","get_DigitalMultiplier method","IVideoProcAmp.get_DigitalMultiplier","IVideoProcAmp::get_DigitalMultiplier","IVideoProcAmpget_DigitalMultiplier","dshow.ivideoprocamp_get_digitalmultiplier","get_DigitalMultiplier","get_DigitalMultiplier method [DirectShow]","get_DigitalMultiplier method [DirectShow]","IVideoProcAmp interface","vidcap/IVideoProcAmp::get_DigitalMultiplier"]
old-location: dshow\ivideoprocamp_get_digitalmultiplier.htm
tech.root: dshow
ms.assetid: 0b7ab1a3-193c-4682-af35-ae0cc5f28f45
ms.date: 12/05/2018
ms.keywords: IVideoProcAmp interface [DirectShow],get_DigitalMultiplier method, IVideoProcAmp.get_DigitalMultiplier, IVideoProcAmp::get_DigitalMultiplier, IVideoProcAmpget_DigitalMultiplier, dshow.ivideoprocamp_get_digitalmultiplier, get_DigitalMultiplier, get_DigitalMultiplier method [DirectShow], get_DigitalMultiplier method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::get_DigitalMultiplier
req.header: vidcap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
 - IVideoProcAmp::get_DigitalMultiplier
 - vidcap/IVideoProcAmp::get_DigitalMultiplier
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vidcap.h
api_name:
 - IVideoProcAmp.get_DigitalMultiplier
---

# IVideoProcAmp::get_DigitalMultiplier


## -description

The <code>get_DigitalMultiplier</code> method returns the camera's digital zoom level.

## -parameters

### -param pValue [out]

Receives the digital zoom multiplier.

### -param pFlags [out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-videoprocampflags">VideoProcAmpFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

Digital zoom is applied after the image is captured. The effect of digital zoom is to multiply the optical magnification by a factor <i>m</i>, which can be calculated as follows:


```cpp

m = ( (Z'cur - Z'min) * (m-max - 1) ) / (Z'max - Z'min) ) + 1

```


where

<ul>
<li>
            Z'cur = Current digital zoom level.</li>
<li>
            Z'min, Z'max = Minimum and maximum digital zoom. See <a href="/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-getrange_digitalmultiplier">IVideoProcAmp::getRange_DigitalMultiplier</a>.</li>
<li>
            m-max = Maximum digital magnification. See KSPROPERTY_VIDEOPROCAMP_DIGITAL_MULTIPLIER_LIMIT, documented in the Windows DDK.</li>
</ul>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-get_focallengths">ICameraControl::get_FocalLengths</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-ivideoprocamp">IVideoProcAmp Interface</a>