---
UID: NF:strmif.IOverlay.Unadvise
title: IOverlay::Unadvise (strmif.h)
author: windows-sdk-content
description: The Unadvise method terminates the advise link established with the IOverlayNotify interface.
old-location: dshow\ioverlay_unadvise.htm
tech.root: DirectShow
ms.assetid: da987152-d5cd-42c5-848a-6d70ad25ca33
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOverlay interface [DirectShow],Unadvise method, IOverlay.Unadvise, IOverlay::Unadvise, IOverlayUnadvise, Unadvise, Unadvise method [DirectShow], Unadvise method [DirectShow],IOverlay interface, dshow.ioverlay_unadvise, strmif/IOverlay::Unadvise
ms.topic: method
f1_keywords: 
 - "strmif/IOverlay.Unadvise"
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
 - IOverlay.Unadvise
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOverlay::Unadvise


## -description



The <code>Unadvise</code> method terminates the advise link established with the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ioverlaynotify">IOverlayNotify</a> interface.




## -parameters






## -returns



Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.




## -remarks



This method terminates the advise link established by using the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ioverlay-advise">IOverlay::Advise</a> method. Only one advise link can be maintained at any one time.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ioverlay">IOverlay Interface</a>
 

 

