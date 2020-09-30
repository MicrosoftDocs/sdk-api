---
UID: NF:dxgi1_2.IDXGIOutputDuplication.AcquireNextFrame
title: IDXGIOutputDuplication::AcquireNextFrame (dxgi1_2.h)
description: Indicates that the application is ready to process the next desktop image.
helpviewer_keywords: ["AcquireNextFrame","AcquireNextFrame method [DXGI]","AcquireNextFrame method [DXGI]","IDXGIOutputDuplication interface","IDXGIOutputDuplication interface [DXGI]","AcquireNextFrame method","IDXGIOutputDuplication.AcquireNextFrame","IDXGIOutputDuplication::AcquireNextFrame","direct3ddxgi.idxgioutputduplication_acquirenextframe","dxgi1_2/IDXGIOutputDuplication::AcquireNextFrame"]
old-location: direct3ddxgi\idxgioutputduplication_acquirenextframe.htm
tech.root: direct3ddxgi
ms.assetid: C4F8C462-C8D8-4418-9543-7C8C32CE9498
ms.date: 12/05/2018
ms.keywords: AcquireNextFrame, AcquireNextFrame method [DXGI], AcquireNextFrame method [DXGI],IDXGIOutputDuplication interface, IDXGIOutputDuplication interface [DXGI],AcquireNextFrame method, IDXGIOutputDuplication.AcquireNextFrame, IDXGIOutputDuplication::AcquireNextFrame, direct3ddxgi.idxgioutputduplication_acquirenextframe, dxgi1_2/IDXGIOutputDuplication::AcquireNextFrame
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dxgi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIOutputDuplication::AcquireNextFrame
 - dxgi1_2/IDXGIOutputDuplication::AcquireNextFrame
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGIOutputDuplication.AcquireNextFrame
---

# IDXGIOutputDuplication::AcquireNextFrame


## -description

Indicates that the application is ready to process the next desktop image.

## -parameters

### -param TimeoutInMilliseconds [in]

The time-out interval, in milliseconds. This interval specifies the amount of time that this method waits for a new frame before it returns to the caller.  This method returns if the interval elapses, and a new desktop image is not available.

For more information about the time-out interval, see Remarks.

### -param pFrameInfo [out]

A pointer to a memory location that receives the <a href="/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_outdupl_frame_info">DXGI_OUTDUPL_FRAME_INFO</a> structure that describes timing and presentation statistics for a frame.

### -param ppDesktopResource [out]

A pointer to a variable that receives the <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiresource">IDXGIResource</a> interface of the surface that contains the desktop bitmap.

## -returns

<b>AcquireNextFrame</b> returns:
        <ul>
<li>S_OK if it successfully received the next desktop image.</li>
<li>DXGI_ERROR_ACCESS_LOST if the desktop duplication interface is invalid. The desktop duplication interface typically becomes invalid when a different type of image is displayed on the desktop.  Examples of this situation are: <ul>
<li>Desktop switch</li>
<li>Mode change</li>
<li>Switch from DWM on, DWM off, or other full-screen application</li>
</ul>In this situation, the application must release the <a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutputduplication">IDXGIOutputDuplication</a> interface and create a new <b>IDXGIOutputDuplication</b> for the new content.</li>
<li>DXGI_ERROR_WAIT_TIMEOUT if the time-out interval elapsed before the next desktop frame was available.</li>
<li>DXGI_ERROR_INVALID_CALL if the application called <b>AcquireNextFrame</b> without releasing the previous frame.</li>
<li>E_INVALIDARG if one of the parameters to <b>AcquireNextFrame</b> is incorrect; for example, if <i>pFrameInfo</i> is NULL.</li>
<li>Possibly other error codes that are described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic.</li>
</ul>

## -remarks

When <b>AcquireNextFrame</b> returns successfully, the calling application can access the desktop image that <b>AcquireNextFrame</b> returns in the variable at <i>ppDesktopResource</i>.
If the caller specifies a zero time-out interval in the <i>TimeoutInMilliseconds</i> parameter, <b>AcquireNextFrame</b> verifies whether there is a new desktop image available, returns immediately, and indicates its outcome with the return value.  If the caller specifies an <b>INFINITE</b> time-out interval in the <i>TimeoutInMilliseconds</i> parameter, the time-out interval never elapses.

<div class="alert"><b>Note</b>  You cannot cancel the wait that you specified in the <i>TimeoutInMilliseconds</i> parameter. Therefore, if you must periodically check for other conditions (for example, a terminate signal), you should specify a non-<b>INFINITE</b> time-out interval. After the time-out interval elapses, you can check for these other conditions and then call <b>AcquireNextFrame</b> again to wait for the next frame.</div>
<div> </div>
<b>AcquireNextFrame</b> acquires a new desktop frame when the operating system either updates the desktop bitmap image or changes the shape or position of a hardware pointer.  The new frame that <b>AcquireNextFrame</b> acquires might have only the desktop image updated, only the pointer shape or position updated, or both.

## -see-also

<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutputduplication">IDXGIOutputDuplication</a>