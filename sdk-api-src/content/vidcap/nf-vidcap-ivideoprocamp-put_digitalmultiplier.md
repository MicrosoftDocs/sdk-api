---
UID: NF:vidcap.IVideoProcAmp.put_DigitalMultiplier
title: IVideoProcAmp::put_DigitalMultiplier (vidcap.h)
description: The put_DigitalMultiplier method sets the camera's digital zoom level.
helpviewer_keywords: ["IVideoProcAmp interface [DirectShow]","put_DigitalMultiplier method","IVideoProcAmp.put_DigitalMultiplier","IVideoProcAmp::put_DigitalMultiplier","IVideoProcAmpput_DigitalMultiplier","dshow.ivideoprocamp_put_digitalmultiplier","put_DigitalMultiplier","put_DigitalMultiplier method [DirectShow]","put_DigitalMultiplier method [DirectShow]","IVideoProcAmp interface","vidcap/IVideoProcAmp::put_DigitalMultiplier"]
old-location: dshow\ivideoprocamp_put_digitalmultiplier.htm
tech.root: dshow
ms.assetid: c1832aad-22fc-41f0-a99a-09b56c148384
ms.date: 12/05/2018
ms.keywords: IVideoProcAmp interface [DirectShow],put_DigitalMultiplier method, IVideoProcAmp.put_DigitalMultiplier, IVideoProcAmp::put_DigitalMultiplier, IVideoProcAmpput_DigitalMultiplier, dshow.ivideoprocamp_put_digitalmultiplier, put_DigitalMultiplier, put_DigitalMultiplier method [DirectShow], put_DigitalMultiplier method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::put_DigitalMultiplier
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
 - IVideoProcAmp::put_DigitalMultiplier
 - vidcap/IVideoProcAmp::put_DigitalMultiplier
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
 - IVideoProcAmp.put_DigitalMultiplier
---

# IVideoProcAmp::put_DigitalMultiplier


## -description

The <code>put_DigitalMultiplier</code> method sets the camera's digital zoom level.

## -parameters

### -param Value [in]

Specifies the digital zoom multiplier.

### -param Flags [in]

Zero or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-videoprocampflags">VideoProcAmpFlags</a>. If the VideoProcAmp_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

For more information about the digital zoom multiplier, see <a href="/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-get_digitalmultiplier">IVideoProcAmp::get_DigitalMultiplier</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-ivideoprocamp">IVideoProcAmp Interface</a>