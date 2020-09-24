---
UID: NS:dxgi.DXGI_SHARED_RESOURCE
title: DXGI_SHARED_RESOURCE (dxgi.h)
description: Represents a handle to a shared resource.
helpviewer_keywords: ["DXGI_SHARED_RESOURCE","DXGI_SHARED_RESOURCE structure [DXGI]","aa3179a5-6a16-4e5d-df66-783c4edeb8f4","direct3ddxgi.dxgi_shared_resource","dxgi/DXGI_SHARED_RESOURCE"]
old-location: direct3ddxgi\dxgi_shared_resource.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\dxgi_shared_resource.htm
ms.date: 12/05/2018
ms.keywords: DXGI_SHARED_RESOURCE, DXGI_SHARED_RESOURCE structure [DXGI], aa3179a5-6a16-4e5d-df66-783c4edeb8f4, direct3ddxgi.dxgi_shared_resource, dxgi/DXGI_SHARED_RESOURCE
req.header: dxgi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DXGI_SHARED_RESOURCE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_SHARED_RESOURCE
 - dxgi/DXGI_SHARED_RESOURCE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGI.h
api_name:
 - DXGI_SHARED_RESOURCE
---

# DXGI_SHARED_RESOURCE structure


## -description

Represents a handle to a shared resource.

## -struct-fields

### -field Handle

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HANDLE</a></b>

A handle to a shared resource.

## -remarks

To create a shared surface, pass a shared-resource handle into the <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-createsurface">IDXGIDevice::CreateSurface</a> method.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-structures">DXGI Structures</a>