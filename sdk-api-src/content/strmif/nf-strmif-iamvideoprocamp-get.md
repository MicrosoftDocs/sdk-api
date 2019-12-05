---
UID: NF:strmif.IAMVideoProcAmp.Get
title: IAMVideoProcAmp::Get (strmif.h)
description: The Get method gets the current setting of a video property.
old-location: dshow\iamvideoprocamp_get.htm
tech.root: DirectShow
ms.assetid: 8924383e-23e1-4732-9eff-dc7c8d0e361a
ms.date: 12/05/2018
ms.keywords: Get, Get method [DirectShow], Get method [DirectShow],IAMVideoProcAmp interface, IAMVideoProcAmp interface [DirectShow],Get method, IAMVideoProcAmp.Get, IAMVideoProcAmp::Get, IAMVideoProcAmpGet, dshow.iamvideoprocamp_get, strmif/IAMVideoProcAmp::Get
ms.topic: method
f1_keywords:
- strmif/IAMVideoProcAmp.Get
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IAMVideoProcAmp.Get
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMVideoProcAmp::Get


## -description



The <code>Get</code> method gets the current setting of a video property.




## -parameters




### -param Property [in]

Specifies the property to retrieve, as a value from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-videoprocampproperty">VideoProcAmpProperty</a> enumeration.
          


### -param lValue [out]

Receives the value of the property.
          


### -param Flags [out]

Receives a member of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-videoprocampflags">VideoProcAmpFlags</a> enumeration. The returned value indicates whether the setting is controlled manually or automatically.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/configure-the-video-quality">Configure the Video Quality</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamvideoprocamp">IAMVideoProcAmp Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamvideoprocamp-set">IAMVideoProcAmp::Set</a>
 

 

