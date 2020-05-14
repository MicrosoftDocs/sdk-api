---
UID: NF:strmif.IOverlay.GetColorKey
title: IOverlay::GetColorKey (strmif.h)
description: The GetColorKey method retrieves the current color key used for chroma keying.helpviewer_keywords: ["GetColorKey","GetColorKey method [DirectShow]","GetColorKey method [DirectShow]","IOverlay interface","IOverlay interface [DirectShow]","GetColorKey method","IOverlay.GetColorKey","IOverlay::GetColorKey","IOverlayGetColorKey","dshow.ioverlay_getcolorkey","strmif/IOverlay::GetColorKey"]
old-location: dshow\ioverlay_getcolorkey.htm
tech.root: DirectShow
ms.assetid: fc9e414e-be53-46e7-b329-23f17fc23725
ms.date: 12/05/2018
ms.keywords: GetColorKey, GetColorKey method [DirectShow], GetColorKey method [DirectShow],IOverlay interface, IOverlay interface [DirectShow],GetColorKey method, IOverlay.GetColorKey, IOverlay::GetColorKey, IOverlayGetColorKey, dshow.ioverlay_getcolorkey, strmif/IOverlay::GetColorKey
f1_keywords:
- strmif/IOverlay.GetColorKey
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
- IOverlay.GetColorKey
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOverlay::GetColorKey


## -description



The <code>GetColorKey</code> method retrieves the current color key used for chroma keying.




## -parameters




### -param pColorKey [out]

Pointer to a variable that receives the current color key for chroma keying.


## -returns



Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.




## -remarks



If you change the color key by using the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ioverlay-setcolorkey">IOverlay::SetColorKey</a> method, all the advise links receive an <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ioverlaynotify-oncolorkeychange">IOverlayNotify::OnColorKeyChange</a> callback method with the new color.

If no color key is currently being used, this method returns VFW_E_NO_COLOR_KEY_SET.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ioverlay">IOverlay Interface</a>
 

 

