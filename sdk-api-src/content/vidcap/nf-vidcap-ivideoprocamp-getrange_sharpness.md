---
UID: NF:vidcap.IVideoProcAmp.getRange_Sharpness
title: IVideoProcAmp::getRange_Sharpness (vidcap.h)
author: windows-sdk-content
description: The getRange_Sharpness method returns the range of sharpness settings supported by the camera.
old-location: dshow\ivideoprocamp_getrange_sharpness.htm
tech.root: DirectShow
ms.assetid: 9a5fe298-e76b-44ac-9fcd-a5d1aeb3593c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVideoProcAmp interface [DirectShow],getRange_Sharpness method, IVideoProcAmp.getRange_Sharpness, IVideoProcAmp::getRange_Sharpness, IVideoProcAmpgetRange_Sharpness, dshow.ivideoprocamp_getrange_sharpness, getRange_Sharpness, getRange_Sharpness method [DirectShow], getRange_Sharpness method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::getRange_Sharpness
ms.topic: method
f1_keywords: 
 - "vidcap/IVideoProcAmp.getRange_Sharpness"
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
 - IVideoProcAmp.getRange_Sharpness
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVideoProcAmp::getRange_Sharpness


## -description


The <code>getRange_Sharpness</code> method returns the range of sharpness settings supported by the camera.


## -parameters




### -param pMin [out]

Receives the minimum sharpness setting.


### -param pMax [out]

Receives the maximum sharpness setting.


### -param pSteppingDelta [out]

Receives the smallest step between settings.


### -param pDefault [out]

Receives the default sharpness setting.


### -param pCapsFlag [out]

Receives one or more flags. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-videoprocampflags">VideoProcAmpFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nn-vidcap-ivideoprocamp">IVideoProcAmp Interface</a>
 

 

