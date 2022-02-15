---
UID: NF:dxgi1_2.IDXGIOutputDuplication.UnMapDesktopSurface
title: IDXGIOutputDuplication::UnMapDesktopSurface (dxgi1_2.h)
description: Invalidates the pointer to the desktop image that was retrieved by using IDXGIOutputDuplication::MapDesktopSurface.
helpviewer_keywords: ["IDXGIOutputDuplication interface [DXGI]","UnMapDesktopSurface method","IDXGIOutputDuplication.UnMapDesktopSurface","IDXGIOutputDuplication::UnMapDesktopSurface","UnMapDesktopSurface","UnMapDesktopSurface method [DXGI]","UnMapDesktopSurface method [DXGI]","IDXGIOutputDuplication interface","direct3ddxgi.idxgioutputduplication_unmapdesktopsurface","dxgi1_2/IDXGIOutputDuplication::UnMapDesktopSurface"]
old-location: direct3ddxgi\idxgioutputduplication_unmapdesktopsurface.htm
tech.root: direct3ddxgi
ms.assetid: 1B9AF088-5856-4F1C-A794-6CF870D62A29
ms.date: 12/05/2018
ms.keywords: IDXGIOutputDuplication interface [DXGI],UnMapDesktopSurface method, IDXGIOutputDuplication.UnMapDesktopSurface, IDXGIOutputDuplication::UnMapDesktopSurface, UnMapDesktopSurface, UnMapDesktopSurface method [DXGI], UnMapDesktopSurface method [DXGI],IDXGIOutputDuplication interface, direct3ddxgi.idxgioutputduplication_unmapdesktopsurface, dxgi1_2/IDXGIOutputDuplication::UnMapDesktopSurface
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
 - IDXGIOutputDuplication::UnMapDesktopSurface
 - dxgi1_2/IDXGIOutputDuplication::UnMapDesktopSurface
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
 - IDXGIOutputDuplication.UnMapDesktopSurface
---

# IDXGIOutputDuplication::UnMapDesktopSurface


## -description

Invalidates the pointer to the desktop image that was retrieved by using <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutputduplication-mapdesktopsurface">IDXGIOutputDuplication::MapDesktopSurface</a>.



## -returns

<b>UnMapDesktopSurface</b> returns:
        <ul>
<li>S_OK if it successfully completed.</li>
<li>DXGI_ERROR_INVALID_CALL if the application did not map the desktop surface by calling <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutputduplication-mapdesktopsurface">IDXGIOutputDuplication::MapDesktopSurface</a>.</li>
<li>Possibly other error codes that are described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutputduplication">IDXGIOutputDuplication</a>
