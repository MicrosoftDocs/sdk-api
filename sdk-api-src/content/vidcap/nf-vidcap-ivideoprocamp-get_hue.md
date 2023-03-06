---
UID: NF:vidcap.IVideoProcAmp.get_Hue
title: IVideoProcAmp::get_Hue (vidcap.h)
description: The get_Hue method returns the camera's hue setting.
helpviewer_keywords: ["IVideoProcAmp interface [DirectShow]","get_Hue method","IVideoProcAmp.get_Hue","IVideoProcAmp::get_Hue","IVideoProcAmpget_Hue","dshow.ivideoprocamp_get_hue","get_Hue","get_Hue method [DirectShow]","get_Hue method [DirectShow]","IVideoProcAmp interface","vidcap/IVideoProcAmp::get_Hue"]
old-location: dshow\ivideoprocamp_get_hue.htm
tech.root: dshow
ms.assetid: dfdd44b5-fd39-40da-95b8-9008aef10f9a
ms.date: 12/05/2018
ms.keywords: IVideoProcAmp interface [DirectShow],get_Hue method, IVideoProcAmp.get_Hue, IVideoProcAmp::get_Hue, IVideoProcAmpget_Hue, dshow.ivideoprocamp_get_hue, get_Hue, get_Hue method [DirectShow], get_Hue method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::get_Hue
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
 - IVideoProcAmp::get_Hue
 - vidcap/IVideoProcAmp::get_Hue
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
 - IVideoProcAmp.get_Hue
---

# IVideoProcAmp::get_Hue


## -description

The <code>get_Hue</code> method returns the camera's hue setting.

## -parameters

### -param pValue [out]

Receives the hue setting, in units of degrees * 100. Theoretical values range from –180 degrees to +180 degrees, but the actual range depends on the camera. See <a href="/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-getrange_hue">IVideoProcAmp::getRange_Hue</a>.

### -param pFlags [out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-videoprocampflags">VideoProcAmpFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-ivideoprocamp">IVideoProcAmp Interface</a>