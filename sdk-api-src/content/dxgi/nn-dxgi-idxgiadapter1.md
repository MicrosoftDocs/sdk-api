---
UID: NN:dxgi.IDXGIAdapter1
title: IDXGIAdapter1 (dxgi.h)
description: The IDXGIAdapter1 interface represents a display sub-system (including one or more GPU's, DACs and video memory).
helpviewer_keywords: ["2ac7b82f-b5a5-ec94-1506-33b758455dd2","IDXGIAdapter1","IDXGIAdapter1 interface [DXGI]","IDXGIAdapter1 interface [DXGI]","described","direct3ddxgi.idxgiadapter1","dxgi/IDXGIAdapter1"]
old-location: direct3ddxgi\idxgiadapter1.htm
tech.root: direct3ddxgi
ms.assetid: 003d5a10-e978-481f-8ca6-9e5ab69bfec0
ms.date: 12/05/2018
ms.keywords: 2ac7b82f-b5a5-ec94-1506-33b758455dd2, IDXGIAdapter1, IDXGIAdapter1 interface [DXGI], IDXGIAdapter1 interface [DXGI],described, direct3ddxgi.idxgiadapter1, dxgi/IDXGIAdapter1
req.header: dxgi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: DXGI.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIAdapter1
 - dxgi/IDXGIAdapter1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGIAdapter1
---

# IDXGIAdapter1 interface


## -description

The <b>IDXGIAdapter1</b> interface represents a display sub-system (including one or more GPU's, DACs and video memory).

## -inheritance

The <b>IDXGIAdapter1</b> interface inherits from <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter">IDXGIAdapter</a>. <b>IDXGIAdapter1</b> also has these types of members:

## -remarks

This interface is not supported by DXGI 1.0, which shipped in Windows Vista and Windows Server 2008. DXGI 1.1 support is required, which is available on
            Windows 7, Windows Server 2008 R2, and as an update to Windows Vista with Service Pack 2 (SP2) (<a href="https://support.microsoft.com/topic/application-compatibility-update-for-windows-vista-windows-server-2008-windows-7-and-windows-server-2008-r2-february-2010-3eb7848b-9a76-85fe-98d0-729e3827ea60">KB 971644</a>) and Windows Server 2008 (<a href="https://support.microsoft.com/kb/971512/">KB 971512</a>).
          

A display sub-system is often referred to as a video card, however, on some machines the display sub-system is part of the mother board.

To enumerate the display sub-systems, use <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory1-enumadapters1">IDXGIFactory1::EnumAdapters1</a>. To get an interface to the adapter for a
            particular device, use <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-getadapter">IDXGIDevice::GetAdapter</a>. To create a software adapter, use <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createsoftwareadapter">IDXGIFactory::CreateSoftwareAdapter</a>.
          

<b>Windows Phone 8:
        </b> This API is supported.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter">IDXGIAdapter</a>
