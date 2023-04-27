---
UID: NF:vidcap.IVideoProcAmp.get_WhiteBalance
title: IVideoProcAmp::get_WhiteBalance (vidcap.h)
description: The get_WhiteBalance method returns the camera's white balance, specified as a color temperature.
helpviewer_keywords: ["IVideoProcAmp interface [DirectShow]","get_WhiteBalance method","IVideoProcAmp.get_WhiteBalance","IVideoProcAmp::get_WhiteBalance","IVideoProcAmpget_WhiteBalance","dshow.ivideoprocamp_get_whitebalance","get_WhiteBalance","get_WhiteBalance method [DirectShow]","get_WhiteBalance method [DirectShow]","IVideoProcAmp interface","vidcap/IVideoProcAmp::get_WhiteBalance"]
old-location: dshow\ivideoprocamp_get_whitebalance.htm
tech.root: dshow
ms.assetid: 53743bff-4257-4abf-b41a-aa5586ab37b5
ms.date: 12/05/2018
ms.keywords: IVideoProcAmp interface [DirectShow],get_WhiteBalance method, IVideoProcAmp.get_WhiteBalance, IVideoProcAmp::get_WhiteBalance, IVideoProcAmpget_WhiteBalance, dshow.ivideoprocamp_get_whitebalance, get_WhiteBalance, get_WhiteBalance method [DirectShow], get_WhiteBalance method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::get_WhiteBalance
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
 - IVideoProcAmp::get_WhiteBalance
 - vidcap/IVideoProcAmp::get_WhiteBalance
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
 - IVideoProcAmp.get_WhiteBalance
---

# IVideoProcAmp::get_WhiteBalance


## -description

The <code>get_WhiteBalance</code> method returns the camera's white balance, specified as a color temperature.

## -parameters

### -param pValue [out]

Receives the white balance, in degrees Kelvin.

### -param pFlags [out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-videoprocampflags">VideoProcAmpFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-ivideoprocamp">IVideoProcAmp Interface</a>