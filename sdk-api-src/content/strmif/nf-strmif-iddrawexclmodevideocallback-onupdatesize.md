---
UID: NF:strmif.IDDrawExclModeVideoCallback.OnUpdateSize
title: IDDrawExclModeVideoCallback::OnUpdateSize (strmif.h)
description: The OnUpdateSize method informs the application that the size of the video rectangle is about to change.helpviewer_keywords: ["IDDrawExclModeVideoCallback interface [DirectShow]","OnUpdateSize method","IDDrawExclModeVideoCallback.OnUpdateSize","IDDrawExclModeVideoCallback::OnUpdateSize","IDDrawExclModeVideoCallbackOnUpdateSize","OnUpdateSize","OnUpdateSize method [DirectShow]","OnUpdateSize method [DirectShow]","IDDrawExclModeVideoCallback interface","dshow.iddrawexclmodevideocallback_onupdatesize","strmif/IDDrawExclModeVideoCallback::OnUpdateSize"]
old-location: dshow\iddrawexclmodevideocallback_onupdatesize.htm
tech.root: DirectShow
ms.assetid: 00ddf110-8efc-414f-abfa-d6c7a22751a8
ms.date: 12/05/2018
ms.keywords: IDDrawExclModeVideoCallback interface [DirectShow],OnUpdateSize method, IDDrawExclModeVideoCallback.OnUpdateSize, IDDrawExclModeVideoCallback::OnUpdateSize, IDDrawExclModeVideoCallbackOnUpdateSize, OnUpdateSize, OnUpdateSize method [DirectShow], OnUpdateSize method [DirectShow],IDDrawExclModeVideoCallback interface, dshow.iddrawexclmodevideocallback_onupdatesize, strmif/IDDrawExclModeVideoCallback::OnUpdateSize
f1_keywords:
- strmif/IDDrawExclModeVideoCallback.OnUpdateSize
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
- IDDrawExclModeVideoCallback.OnUpdateSize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDDrawExclModeVideoCallback::OnUpdateSize


## -description



The <code>OnUpdateSize</code> method informs the application that the size of the video rectangle is about to change.




## -parameters




### -param dwWidth [in]

The new width, in pixels, of the video stream.


### -param dwHeight [in]

The new height, in pixels, of the video stream.


### -param dwARWidth [in]

The new horizontal value of the aspect ratio.


### -param dwARHeight [in]

The new vertical value of the aspect ratio.


## -returns



Returns an HRESULT value.




## -remarks



This method is called when the size of the rectangle in the video stream changes, for example from 704x480 to 640x480.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iddrawexclmodevideocallback">IDDrawExclModeVideoCallback Interface</a>
 

 

