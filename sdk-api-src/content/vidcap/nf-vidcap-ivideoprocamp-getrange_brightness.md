---
UID: NF:vidcap.IVideoProcAmp.getRange_Brightness
title: IVideoProcAmp::getRange_Brightness (vidcap.h)
author: windows-sdk-content
description: The getRange_Brightness method returns the range of brightness settings supported by the camera.
old-location: dshow\ivideoprocamp_getrange_brightness.htm
tech.root: DirectShow
ms.assetid: 236f919a-5ed3-4ce4-877e-023af1a4e4d0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVideoProcAmp interface [DirectShow],getRange_Brightness method, IVideoProcAmp.getRange_Brightness, IVideoProcAmp::getRange_Brightness, IVideoProcAmpgetRange_Brightness, dshow.ivideoprocamp_getrange_brightness, getRange_Brightness, getRange_Brightness method [DirectShow], getRange_Brightness method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::getRange_Brightness
ms.topic: method
f1_keywords: 
 - "vidcap/IVideoProcAmp.getRange_Brightness"
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
 - IVideoProcAmp.getRange_Brightness
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVideoProcAmp::getRange_Brightness


## -description


The <code>getRange_Brightness</code> method returns the range of brightness settings supported by the camera.


## -parameters




### -param pMin [out]

Receives the minimum brightness setting.


### -param pMax [out]

Receives the maximum brightness setting.


### -param pSteppingDelta [out]

Receives the smallest step between settings.


### -param pDefault [out]

Receives the default brightness setting.


### -param pCapsFlag [out]

Receives one or more flags. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-videoprocampflags">VideoProcAmpFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nn-vidcap-ivideoprocamp">IVideoProcAmp Interface</a>
 

 

