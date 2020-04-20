---
UID: NF:amvideo.IFullScreenVideoEx.SetDefault
title: IFullScreenVideoEx::SetDefault (amvideo.h)
description: The SetDefault method saves the current settings.helpviewer_keywords: ["IFullScreenVideoEx interface [DirectShow]","SetDefault method","IFullScreenVideoEx.SetDefault","IFullScreenVideoEx::SetDefault","IFullScreenVideoSetDefault","SetDefault","SetDefault method [DirectShow]","SetDefault method [DirectShow]","IFullScreenVideoEx interface","amvideo/IFullScreenVideoEx::SetDefault","dshow.ifullscreenvideoex_setdefault"]
old-location: dshow\ifullscreenvideoex_setdefault.htm
tech.root: DirectShow
ms.assetid: 1821703c-0da1-4b3e-a921-a66770b8ee0d
ms.date: 12/05/2018
ms.keywords: IFullScreenVideoEx interface [DirectShow],SetDefault method, IFullScreenVideoEx.SetDefault, IFullScreenVideoEx::SetDefault, IFullScreenVideoSetDefault, SetDefault, SetDefault method [DirectShow], SetDefault method [DirectShow],IFullScreenVideoEx interface, amvideo/IFullScreenVideoEx::SetDefault, dshow.ifullscreenvideoex_setdefault
f1_keywords:
- amvideo/IFullScreenVideoEx.SetDefault
dev_langs:
- c++
req.header: amvideo.h
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
- IFullScreenVideoEx.SetDefault
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFullScreenVideoEx::SetDefault


## -description



The <code>SetDefault</code> method saves the current settings.




## -parameters






## -returns



Returns an <b>HRESULT</b> value.




## -remarks



Normally, the properties set through this interface apply only to the current instance of the Full Screen Renderer. Calling this method saves the current values as the global default. This method persists the following information:

<ul>
<li>The clip factor.</li>
<li>The enabled flag for each display mode.</li>
</ul>
It does not persist the caption or the hide-when-deactivated flag.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nn-amvideo-ifullscreenvideoex">IFullScreenVideoEx Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nf-amvideo-ifullscreenvideoex-hideondeactivate">IFullScreenVideoEx::HideOnDeactivate</a>



<a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nf-amvideo-ifullscreenvideoex-setcaption">IFullScreenVideoEx::SetCaption</a>



<a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nf-amvideo-ifullscreenvideoex-setclipfactor">IFullScreenVideoEx::SetClipFactor</a>



<a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nf-amvideo-ifullscreenvideoex-setenabled">IFullScreenVideoEx::SetEnabled</a>
 

 

