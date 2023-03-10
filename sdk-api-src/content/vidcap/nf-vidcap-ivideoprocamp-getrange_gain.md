---
UID: NF:vidcap.IVideoProcAmp.getRange_Gain
title: IVideoProcAmp::getRange_Gain (vidcap.h)
description: The getRange_Gain method returns the range of gain settings supported by the camera.
helpviewer_keywords: ["IVideoProcAmp interface [DirectShow]","getRange_Gain method","IVideoProcAmp.getRange_Gain","IVideoProcAmp::getRange_Gain","IVideoProcAmpgetRange_Gain","dshow.ivideoprocamp_getrange_gain","getRange_Gain","getRange_Gain method [DirectShow]","getRange_Gain method [DirectShow]","IVideoProcAmp interface","vidcap/IVideoProcAmp::getRange_Gain"]
old-location: dshow\ivideoprocamp_getrange_gain.htm
tech.root: dshow
ms.assetid: a039cece-ee44-43e0-ade9-5a7e1d9a1c11
ms.date: 12/05/2018
ms.keywords: IVideoProcAmp interface [DirectShow],getRange_Gain method, IVideoProcAmp.getRange_Gain, IVideoProcAmp::getRange_Gain, IVideoProcAmpgetRange_Gain, dshow.ivideoprocamp_getrange_gain, getRange_Gain, getRange_Gain method [DirectShow], getRange_Gain method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::getRange_Gain
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
 - IVideoProcAmp::getRange_Gain
 - vidcap/IVideoProcAmp::getRange_Gain
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
 - IVideoProcAmp.getRange_Gain
---

# IVideoProcAmp::getRange_Gain


## -description

The <code>getRange_Gain</code> method returns the range of gain settings supported by the camera.

## -parameters

### -param pMin [out]

Receives the minimum gain setting.

### -param pMax [out]

Receives the maximum gain setting.

### -param pSteppingDelta [out]

Receives the smallest step between settings.

### -param pDefault [out]

Receives the default gain setting.

### -param pCapsFlag [out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-videoprocampflags">VideoProcAmpFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-ivideoprocamp">IVideoProcAmp Interface</a>