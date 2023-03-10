---
UID: NN:dxgi1_2.IDXGIAdapter2
title: IDXGIAdapter2 (dxgi1_2.h)
description: The IDXGIAdapter2 interface represents a display subsystem, which includes one or more GPUs, DACs, and video memory.
helpviewer_keywords: ["IDXGIAdapter2","IDXGIAdapter2 interface [DXGI]","IDXGIAdapter2 interface [DXGI]","described","direct3ddxgi.idxgiadapter2","dxgi1_2/IDXGIAdapter2"]
old-location: direct3ddxgi\idxgiadapter2.htm
tech.root: direct3ddxgi
ms.assetid: 9AAD133C-CE40-498B-827F-2B35C7C15B8C
ms.date: 12/05/2018
ms.keywords: IDXGIAdapter2, IDXGIAdapter2 interface [DXGI], IDXGIAdapter2 interface [DXGI],described, direct3ddxgi.idxgiadapter2, dxgi1_2/IDXGIAdapter2
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - IDXGIAdapter2
 - dxgi1_2/IDXGIAdapter2
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
 - IDXGIAdapter2
---

# IDXGIAdapter2 interface


## -description

The <b>IDXGIAdapter2</b> interface represents a display subsystem, which includes one or more GPUs, DACs, and video memory.

## -inheritance

The <b>IDXGIAdapter2</b> interface inherits from <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter1">IDXGIAdapter1</a>. <b>IDXGIAdapter2</b> also has these types of members:

## -remarks

A display subsystem is often referred to as a video card; however, on some computers, the display subsystem is part of the motherboard.
        

To enumerate the display subsystems, use <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory1-enumadapters1">IDXGIFactory1::EnumAdapters1</a>.
        

To get an interface to the adapter for a particular device, use <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-getadapter">IDXGIDevice::GetAdapter</a>.
        

To create a software adapter, use <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createsoftwareadapter">IDXGIFactory::CreateSoftwareAdapter</a>.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter1">IDXGIAdapter1</a>
