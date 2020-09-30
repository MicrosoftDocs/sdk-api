---
UID: NF:vidcap.IVideoProcAmp.getRange_BacklightCompensation
title: IVideoProcAmp::getRange_BacklightCompensation (vidcap.h)
description: The getRange_BacklightCompensation method returns the range of backlight compensation settings supported by the camera.
helpviewer_keywords: ["IVideoProcAmp interface [DirectShow]","getRange_BacklightCompensation method","IVideoProcAmp.getRange_BacklightCompensation","IVideoProcAmp::getRange_BacklightCompensation","IVideoProcAmpgetRange_BacklightCompensation","dshow.ivideoprocamp_getrange_backlightcompensation","getRange_BacklightCompensation","getRange_BacklightCompensation method [DirectShow]","getRange_BacklightCompensation method [DirectShow]","IVideoProcAmp interface","vidcap/IVideoProcAmp::getRange_BacklightCompensation"]
old-location: dshow\ivideoprocamp_getrange_backlightcompensation.htm
tech.root: dshow
ms.assetid: 4527e7e9-372c-4883-a068-1ce53eb2256a
ms.date: 12/05/2018
ms.keywords: IVideoProcAmp interface [DirectShow],getRange_BacklightCompensation method, IVideoProcAmp.getRange_BacklightCompensation, IVideoProcAmp::getRange_BacklightCompensation, IVideoProcAmpgetRange_BacklightCompensation, dshow.ivideoprocamp_getrange_backlightcompensation, getRange_BacklightCompensation, getRange_BacklightCompensation method [DirectShow], getRange_BacklightCompensation method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::getRange_BacklightCompensation
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
 - IVideoProcAmp::getRange_BacklightCompensation
 - vidcap/IVideoProcAmp::getRange_BacklightCompensation
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
 - IVideoProcAmp.getRange_BacklightCompensation
---

# IVideoProcAmp::getRange_BacklightCompensation


## -description

The <code>getRange_BacklightCompensation</code> method returns the range of backlight compensation settings supported by the camera.

## -parameters

### -param pMin [out]

Receives the minimum backlight compensation setting.

### -param pMax [out]

Receives the maximum backlight compensation setting.

### -param pSteppingDelta [out]

Receives the smallest step between settings.

### -param pDefault [out]

Receives the default backlight compensation setting.

### -param pCapsFlag [out]

Receives one or more flags. See <a href="/previous-versions/windows/desktop/api/strmif/ne-strmif-videoprocampflags">VideoProcAmpFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-ivideoprocamp">IVideoProcAmp Interface</a>