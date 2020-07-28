---
UID: NF:vidcap.IVideoProcAmp.getRange_Gamma
title: IVideoProcAmp::getRange_Gamma (vidcap.h)
description: The getRange_Gamma method returns the range of gamma settings supported by the camera.
helpviewer_keywords: ["IVideoProcAmp interface [DirectShow]","getRange_Gamma method","IVideoProcAmp.getRange_Gamma","IVideoProcAmp::getRange_Gamma","IVideoProcAmpgetRange_Gamma","dshow.ivideoprocamp_getrange_gamma","getRange_Gamma","getRange_Gamma method [DirectShow]","getRange_Gamma method [DirectShow]","IVideoProcAmp interface","vidcap/IVideoProcAmp::getRange_Gamma"]
old-location: dshow\ivideoprocamp_getrange_gamma.htm
tech.root: dshow
ms.assetid: 36914aed-d11c-42c0-a0e5-ba1d3ba6dd22
ms.date: 12/05/2018
ms.keywords: IVideoProcAmp interface [DirectShow],getRange_Gamma method, IVideoProcAmp.getRange_Gamma, IVideoProcAmp::getRange_Gamma, IVideoProcAmpgetRange_Gamma, dshow.ivideoprocamp_getrange_gamma, getRange_Gamma, getRange_Gamma method [DirectShow], getRange_Gamma method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::getRange_Gamma
f1_keywords:
- vidcap/IVideoProcAmp.getRange_Gamma
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Vidcap.h
api_name:
- IVideoProcAmp.getRange_Gamma
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVideoProcAmp::getRange_Gamma


## -description


The <code>getRange_Gamma</code> method returns the range of gamma settings supported by the camera.


## -parameters




### -param pMin [out]

Receives the minimum gamma setting.


### -param pMax [out]

Receives the maximum gamma setting.


### -param pSteppingDelta [out]

Receives the smallest step between settings.


### -param pDefault [out]

Receives the default gamma setting.


### -param pCapsFlag [out]

Receives one or more flags. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-videoprocampflags">VideoProcAmpFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nn-vidcap-ivideoprocamp">IVideoProcAmp Interface</a>
 

 

