---
UID: NF:dxgi1_2.IDXGIOutputDuplication.ReleaseFrame
title: IDXGIOutputDuplication::ReleaseFrame (dxgi1_2.h)
description: Indicates that the application finished processing the frame.
helpviewer_keywords: ["IDXGIOutputDuplication interface [DXGI]","ReleaseFrame method","IDXGIOutputDuplication.ReleaseFrame","IDXGIOutputDuplication::ReleaseFrame","ReleaseFrame","ReleaseFrame method [DXGI]","ReleaseFrame method [DXGI]","IDXGIOutputDuplication interface","direct3ddxgi.idxgioutputduplication_releaseframe","dxgi1_2/IDXGIOutputDuplication::ReleaseFrame"]
old-location: direct3ddxgi\idxgioutputduplication_releaseframe.htm
tech.root: direct3ddxgi
ms.assetid: 841858AA-4840-4B04-B54A-F10362D43F5B
ms.date: 12/05/2018
ms.keywords: IDXGIOutputDuplication interface [DXGI],ReleaseFrame method, IDXGIOutputDuplication.ReleaseFrame, IDXGIOutputDuplication::ReleaseFrame, ReleaseFrame, ReleaseFrame method [DXGI], ReleaseFrame method [DXGI],IDXGIOutputDuplication interface, direct3ddxgi.idxgioutputduplication_releaseframe, dxgi1_2/IDXGIOutputDuplication::ReleaseFrame
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
 - IDXGIOutputDuplication::ReleaseFrame
 - dxgi1_2/IDXGIOutputDuplication::ReleaseFrame
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
 - IDXGIOutputDuplication.ReleaseFrame
---

# IDXGIOutputDuplication::ReleaseFrame


## -description

Indicates that the application finished processing the frame.



## -returns

<b>ReleaseFrame</b> returns:
        <ul>
<li>S_OK if it successfully completed.</li>
<li>DXGI_ERROR_INVALID_CALL if the application already released the frame.</li>
<li>DXGI_ERROR_ACCESS_LOST if the desktop duplication interface is invalid. The desktop duplication interface typically becomes invalid when a different type of image is displayed on the desktop.  Examples of this situation are: <ul>
<li>Desktop switch</li>
<li>Mode change</li>
<li>Switch from DWM on, DWM off, or other full-screen application</li>
</ul>In this situation, the application must release the <a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutputduplication">IDXGIOutputDuplication</a> interface and create a new <b>IDXGIOutputDuplication</b> for the new content.</li>
<li>Possibly other error codes that are described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic.</li>
</ul>

## -remarks

The application must release the frame before it acquires the next frame.  After the frame is released, the surface that contains the desktop bitmap becomes invalid; you will not be able to use the surface in a DirectX graphics operation.

For performance reasons, we recommend that you release the frame just before you call the <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe">IDXGIOutputDuplication::AcquireNextFrame</a> method to acquire the next frame.  When the client does not own the frame, the operating system copies all desktop updates to the surface. This can result in wasted GPU cycles if the operating system updates the same region for each frame that occurs.  When the client acquires the frame, the client is aware of only the final update to this region; therefore, any overlapping updates during previous frames are wasted. When the client acquires a frame, the client owns the surface; therefore, the operating system can track only the updated regions and cannot copy desktop updates to the surface. Because of this behavior, we recommend that you minimize the time between the call to release the current frame and the call to acquire the next frame.

## -see-also

<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutputduplication">IDXGIOutputDuplication</a>
