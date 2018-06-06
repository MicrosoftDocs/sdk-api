---
UID: NF:dxgi1_2.IDXGIOutputDuplication.UnMapDesktopSurface
title: IDXGIOutputDuplication::UnMapDesktopSurface
author: windows-sdk-content
description: Invalidates the pointer to the desktop image that was retrieved by using IDXGIOutputDuplication::MapDesktopSurface.
old-location: direct3ddxgi\idxgioutputduplication_unmapdesktopsurface.htm
old-project: direct3ddxgi
ms.assetid: 1B9AF088-5856-4F1C-A794-6CF870D62A29
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: IDXGIOutputDuplication interface [DXGI],UnMapDesktopSurface method, IDXGIOutputDuplication.UnMapDesktopSurface, IDXGIOutputDuplication::UnMapDesktopSurface, UnMapDesktopSurface, UnMapDesktopSurface method [DXGI], UnMapDesktopSurface method [DXGI],IDXGIOutputDuplication interface, direct3ddxgi.idxgioutputduplication_unmapdesktopsurface, dxgi1_2/IDXGIOutputDuplication::UnMapDesktopSurface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: DXGI_OFFER_RESOURCE_PRIORITY
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
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIOutputDuplication::UnMapDesktopSurface


## -description


Invalidates the pointer to the desktop image that was retrieved by using <a href="https://msdn.microsoft.com/1FFFF954-0AD2-418E-B0CC-D674994C3CCE">IDXGIOutputDuplication::MapDesktopSurface</a>.


## -parameters






## -returns



<b>UnMapDesktopSurface</b> returns:
        <ul>
<li>S_OK if it successfully completed.</li>
<li>DXGI_ERROR_INVALID_CALL if the application did not map the desktop surface by calling <a href="https://msdn.microsoft.com/1FFFF954-0AD2-418E-B0CC-D674994C3CCE">IDXGIOutputDuplication::MapDesktopSurface</a>.</li>
<li>Possibly other error codes that are described in the <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a> topic.</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/02C4EC3D-D97F-4CFC-ABF5-03B44CE6A658">IDXGIOutputDuplication</a>
 

 

