---
UID: NF:dxgi1_2.IDXGIOutputDuplication.MapDesktopSurface
title: IDXGIOutputDuplication::MapDesktopSurface
author: windows-sdk-content
description: Provides the CPU with efficient access to a desktop image if that desktop image is already in system memory.
old-location: direct3ddxgi\idxgioutputduplication_mapdesktopsurface.htm
old-project: direct3ddxgi
ms.assetid: 1FFFF954-0AD2-418E-B0CC-D674994C3CCE
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IDXGIOutputDuplication interface [DXGI],MapDesktopSurface method, IDXGIOutputDuplication.MapDesktopSurface, IDXGIOutputDuplication::MapDesktopSurface, MapDesktopSurface, MapDesktopSurface method [DXGI], MapDesktopSurface method [DXGI],IDXGIOutputDuplication interface, direct3ddxgi.idxgioutputduplication_mapdesktopsurface, dxgi1_2/IDXGIOutputDuplication::MapDesktopSurface
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
 - IDXGIOutputDuplication.MapDesktopSurface
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIOutputDuplication::MapDesktopSurface


## -description


Provides the CPU with efficient access to a desktop image if that desktop image is already in system memory.


## -parameters




### -param pLockedRect [out]

A pointer to a <a href="https://msdn.microsoft.com/library/Bb173063(v=VS.85).aspx">DXGI_MAPPED_RECT</a> structure that receives the surface data that the CPU needs to directly access the surface data. 


## -returns



<b>MapDesktopSurface</b> returns:
        <ul>
<li>S_OK if it successfully retrieved the surface data.</li>
<li>DXGI_ERROR_ACCESS_LOST if the desktop duplication interface is invalid. The desktop duplication interface typically becomes invalid when a different type of image is displayed on the desktop.  Examples of this situation are: <ul>
<li>Desktop switch</li>
<li>Mode change</li>
<li>Switch from DWM on, DWM off, or other full-screen application</li>
</ul>In this situation, the application must release the <a href="https://msdn.microsoft.com/02C4EC3D-D97F-4CFC-ABF5-03B44CE6A658">IDXGIOutputDuplication</a> interface and create a new <b>IDXGIOutputDuplication</b> for the new content.</li>
<li>DXGI_ERROR_INVALID_CALL if the application already has an outstanding map on the desktop image.  The application must call <a href="https://msdn.microsoft.com/1B9AF088-5856-4F1C-A794-6CF870D62A29">UnMapDesktopSurface</a> before it calls <b>MapDesktopSurface</b> again. DXGI_ERROR_INVALID_CALL is also returned if the application did not own the desktop image when it called <b>MapDesktopSurface</b>.</li>
<li>DXGI_ERROR_UNSUPPORTED if the desktop image is not in system memory. In this situation, the application must first transfer the image to a staging surface and then lock the image by calling the <a href="https://msdn.microsoft.com/library/Bb174567(v=VS.85).aspx">IDXGISurface::Map</a> method.</li>
<li>E_INVALIDARG if the <i>pLockedRect</i> parameter is incorrect; for example, if <i>pLockedRect</i> is <b>NULL</b>.</li>
<li>Possibly other error codes that are described in the <a href="https://msdn.microsoft.com/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a> topic.</li>
</ul>





## -remarks



You can successfully call <b>MapDesktopSurface</b> if the  <b>DesktopImageInSystemMemory</b> member of the <a href="https://msdn.microsoft.com/003014E3-4322-4253-8D69-AE315CDFDA75">DXGI_OUTDUPL_DESC</a> structure is set to <b>TRUE</b>. If <b>DesktopImageInSystemMemory</b> is <b>FALSE</b>, <b>MapDesktopSurface</b> returns DXGI_ERROR_UNSUPPORTED. Call <a href="https://msdn.microsoft.com/40D2CF38-1528-48A4-BC0C-5D8CC132D0CB">IDXGIOutputDuplication::GetDesc</a> to retrieve the <b>DXGI_OUTDUPL_DESC</b> structure.




## -see-also




<a href="https://msdn.microsoft.com/02C4EC3D-D97F-4CFC-ABF5-03B44CE6A658">IDXGIOutputDuplication</a>
 

 

