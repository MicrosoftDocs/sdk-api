---
UID: NF:strmif.IDDrawExclModeVideo.SetDrawParameters
title: IDDrawExclModeVideo::SetDrawParameters (strmif.h)
description: The SetDrawParameters method specifies which part of the original video will appear at which position of the screen.
helpviewer_keywords: ["IDDrawExclModeVideo interface [DirectShow]","SetDrawParameters method","IDDrawExclModeVideo.SetDrawParameters","IDDrawExclModeVideo::SetDrawParameters","IDDrawExclModeVideoSetDrawParameters","SetDrawParameters","SetDrawParameters method [DirectShow]","SetDrawParameters method [DirectShow]","IDDrawExclModeVideo interface","dshow.iddrawexclmodevideo_setdrawparameters","strmif/IDDrawExclModeVideo::SetDrawParameters"]
old-location: dshow\iddrawexclmodevideo_setdrawparameters.htm
tech.root: dshow
ms.assetid: e5c2eda5-4276-4906-8098-37bba3fd4e5a
ms.date: 12/05/2018
ms.keywords: IDDrawExclModeVideo interface [DirectShow],SetDrawParameters method, IDDrawExclModeVideo.SetDrawParameters, IDDrawExclModeVideo::SetDrawParameters, IDDrawExclModeVideoSetDrawParameters, SetDrawParameters, SetDrawParameters method [DirectShow], SetDrawParameters method [DirectShow],IDDrawExclModeVideo interface, dshow.iddrawexclmodevideo_setdrawparameters, strmif/IDDrawExclModeVideo::SetDrawParameters
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDDrawExclModeVideo::SetDrawParameters
 - strmif/IDDrawExclModeVideo::SetDrawParameters
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDDrawExclModeVideo.SetDrawParameters
---

# IDDrawExclModeVideo::SetDrawParameters


## -description

The <code>SetDrawParameters</code> method specifies which part of the original video will appear at which position of the screen.

## -parameters

### -param prcSource [in]

Pointer to the <b>RECT</b> structure of the original video.

### -param prcTarget [in]

Pointer to the <b>RECT</b> that indicates where the video will appear on the screen.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iddrawexclmodevideo">IDDrawExclModeVideo Interface</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iddrawexclmodevideocallback">IDDrawExclModeVideoCallback Interface</a>