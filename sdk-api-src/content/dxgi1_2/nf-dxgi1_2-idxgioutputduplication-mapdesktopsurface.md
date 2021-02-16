---
UID: NF:dxgi1_2.IDXGIOutputDuplication.MapDesktopSurface
title: IDXGIOutputDuplication::MapDesktopSurface (dxgi1_2.h)
description: Provides the CPU with efficient access to a desktop image if that desktop image is already in system memory.
helpviewer_keywords: ["IDXGIOutputDuplication interface [DXGI]","MapDesktopSurface method","IDXGIOutputDuplication.MapDesktopSurface","IDXGIOutputDuplication::MapDesktopSurface","MapDesktopSurface","MapDesktopSurface method [DXGI]","MapDesktopSurface method [DXGI]","IDXGIOutputDuplication interface","direct3ddxgi.idxgioutputduplication_mapdesktopsurface","dxgi1_2/IDXGIOutputDuplication::MapDesktopSurface"]
old-location: direct3ddxgi\idxgioutputduplication_mapdesktopsurface.htm
tech.root: direct3ddxgi
ms.assetid: 1FFFF954-0AD2-418E-B0CC-D674994C3CCE
ms.date: 12/05/2018
ms.keywords: IDXGIOutputDuplication interface [DXGI],MapDesktopSurface method, IDXGIOutputDuplication.MapDesktopSurface, IDXGIOutputDuplication::MapDesktopSurface, MapDesktopSurface, MapDesktopSurface method [DXGI], MapDesktopSurface method [DXGI],IDXGIOutputDuplication interface, direct3ddxgi.idxgioutputduplication_mapdesktopsurface, dxgi1_2/IDXGIOutputDuplication::MapDesktopSurface
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
 - IDXGIOutputDuplication::MapDesktopSurface
 - dxgi1_2/IDXGIOutputDuplication::MapDesktopSurface
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
 - IDXGIOutputDuplication.MapDesktopSurface
---

# IDXGIOutputDuplication::MapDesktopSurface


## -description

Provides the CPU with efficient access to a desktop image if that desktop image is already in system memory.

## -parameters

### -param pLockedRect [out]

A pointer to a <a href="/windows/desktop/api/dxgi/ns-dxgi-dxgi_mapped_rect">DXGI_MAPPED_RECT</a> structure that receives the surface data that the CPU needs to directly access the surface data.

## -returns

<b>MapDesktopSurface</b> returns:
        <ul>
<li>S_OK if it successfully retrieved the surface data.</li>
<li>DXGI_ERROR_ACCESS_LOST if the desktop duplication interface is invalid. The desktop duplication interface typically becomes invalid when a different type of image is displayed on the desktop.  Examples of this situation are: <ul>
<li>Desktop switch</li>
<li>Mode change</li>
<li>Switch from DWM on, DWM off, or other full-screen application</li>
</ul>In this situation, the application must release the <a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutputduplication">IDXGIOutputDuplication</a> interface and create a new <b>IDXGIOutputDuplication</b> for the new content.</li>
<li>DXGI_ERROR_INVALID_CALL if the application already has an outstanding map on the desktop image.  The application must call <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutputduplication-unmapdesktopsurface">UnMapDesktopSurface</a> before it calls <b>MapDesktopSurface</b> again. DXGI_ERROR_INVALID_CALL is also returned if the application did not own the desktop image when it called <b>MapDesktopSurface</b>.</li>
<li>DXGI_ERROR_UNSUPPORTED if the desktop image is not in system memory. In this situation, the application must first transfer the image to a staging surface and then lock the image by calling the <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgisurface-map">IDXGISurface::Map</a> method.</li>
<li>E_INVALIDARG if the <i>pLockedRect</i> parameter is incorrect; for example, if <i>pLockedRect</i> is <b>NULL</b>.</li>
<li>Possibly other error codes that are described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic.</li>
</ul>

## -remarks

You can successfully call <b>MapDesktopSurface</b> if the  <b>DesktopImageInSystemMemory</b> member of the <a href="/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_outdupl_desc">DXGI_OUTDUPL_DESC</a> structure is set to <b>TRUE</b>. If <b>DesktopImageInSystemMemory</b> is <b>FALSE</b>, <b>MapDesktopSurface</b> returns DXGI_ERROR_UNSUPPORTED. Call <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutputduplication-getdesc">IDXGIOutputDuplication::GetDesc</a> to retrieve the <b>DXGI_OUTDUPL_DESC</b> structure.

## -see-also

<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutputduplication">IDXGIOutputDuplication</a>