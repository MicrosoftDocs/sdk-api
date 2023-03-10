---
UID: NF:vidcap.IVideoProcAmp.getRange_WhiteBalanceComponent
title: IVideoProcAmp::getRange_WhiteBalanceComponent (vidcap.h)
description: The getRange_WhiteBalanceComponent method returns the range of white balance settings supported by the camera, expressed as red and blue component values.
helpviewer_keywords: ["IVideoProcAmp interface [DirectShow]","getRange_WhiteBalanceComponent method","IVideoProcAmp.getRange_WhiteBalanceComponent","IVideoProcAmp::getRange_WhiteBalanceComponent","IVideoProcAmpgetRange_WhiteBalanceComponent","dshow.ivideoprocamp_getrange_whitebalancecomponent","getRange_WhiteBalanceComponent","getRange_WhiteBalanceComponent method [DirectShow]","getRange_WhiteBalanceComponent method [DirectShow]","IVideoProcAmp interface","vidcap/IVideoProcAmp::getRange_WhiteBalanceComponent"]
old-location: dshow\ivideoprocamp_getrange_whitebalancecomponent.htm
tech.root: dshow
ms.assetid: dec23c5a-3999-4f9b-81f3-2718b38d5835
ms.date: 12/05/2018
ms.keywords: IVideoProcAmp interface [DirectShow],getRange_WhiteBalanceComponent method, IVideoProcAmp.getRange_WhiteBalanceComponent, IVideoProcAmp::getRange_WhiteBalanceComponent, IVideoProcAmpgetRange_WhiteBalanceComponent, dshow.ivideoprocamp_getrange_whitebalancecomponent, getRange_WhiteBalanceComponent, getRange_WhiteBalanceComponent method [DirectShow], getRange_WhiteBalanceComponent method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::getRange_WhiteBalanceComponent
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
 - IVideoProcAmp::getRange_WhiteBalanceComponent
 - vidcap/IVideoProcAmp::getRange_WhiteBalanceComponent
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
 - IVideoProcAmp.getRange_WhiteBalanceComponent
---

# IVideoProcAmp::getRange_WhiteBalanceComponent


## -description

The <code>getRange_WhiteBalanceComponent</code> method returns the range of white balance settings supported by the camera, expressed as red and blue component values.

## -parameters

### -param pMin [out]

Receives the minimum white balance.

### -param pMax [out]

Receives the maximum white balance.

### -param pSteppingDelta [out]

Receives the smallest step between settings.

### -param pDefault [out]

Receives the default white balance.

### -param pCapsFlag [in, out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-videoprocampflags">VideoProcAmpFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-ivideoprocamp">IVideoProcAmp Interface</a>