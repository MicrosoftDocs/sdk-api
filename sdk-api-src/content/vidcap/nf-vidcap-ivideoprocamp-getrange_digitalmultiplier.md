---
UID: NF:vidcap.IVideoProcAmp.getRange_DigitalMultiplier
title: IVideoProcAmp::getRange_DigitalMultiplier (vidcap.h)
description: The getRange_DigitalMultiplier method returns the range of digital zoom levels supported by the camera.
helpviewer_keywords: ["IVideoProcAmp interface [DirectShow]","getRange_DigitalMultiplier method","IVideoProcAmp.getRange_DigitalMultiplier","IVideoProcAmp::getRange_DigitalMultiplier","IVideoProcAmpgetRange_DigitalMultiplier","dshow.ivideoprocamp_getrange_digitalmultiplier","getRange_DigitalMultiplier","getRange_DigitalMultiplier method [DirectShow]","getRange_DigitalMultiplier method [DirectShow]","IVideoProcAmp interface","vidcap/IVideoProcAmp::getRange_DigitalMultiplier"]
old-location: dshow\ivideoprocamp_getrange_digitalmultiplier.htm
tech.root: dshow
ms.assetid: 8a8a5f72-d51f-4f5a-95e4-ac8d1ac1b24f
ms.date: 12/05/2018
ms.keywords: IVideoProcAmp interface [DirectShow],getRange_DigitalMultiplier method, IVideoProcAmp.getRange_DigitalMultiplier, IVideoProcAmp::getRange_DigitalMultiplier, IVideoProcAmpgetRange_DigitalMultiplier, dshow.ivideoprocamp_getrange_digitalmultiplier, getRange_DigitalMultiplier, getRange_DigitalMultiplier method [DirectShow], getRange_DigitalMultiplier method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::getRange_DigitalMultiplier
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
 - IVideoProcAmp::getRange_DigitalMultiplier
 - vidcap/IVideoProcAmp::getRange_DigitalMultiplier
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
 - IVideoProcAmp.getRange_DigitalMultiplier
---

# IVideoProcAmp::getRange_DigitalMultiplier


## -description

The <code>getRange_DigitalMultiplier</code> method returns the range of digital zoom levels supported by the camera.

## -parameters

### -param pMin [out]

Receives the minimum digital zoom level.

### -param pMax [out]

Receives the maximum digital zoom level.

### -param pSteppingDelta [out]

Receives the smallest step between settings.

### -param pDefault [out]

Receives the default digital zoom level.

### -param pCapsFlag [out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-videoprocampflags">VideoProcAmpFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-ivideoprocamp">IVideoProcAmp Interface</a>