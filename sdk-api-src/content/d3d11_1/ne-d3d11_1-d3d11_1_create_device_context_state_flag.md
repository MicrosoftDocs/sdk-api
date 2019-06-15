---
UID: NE:d3d11_1.D3D11_1_CREATE_DEVICE_CONTEXT_STATE_FLAG
title: D3D11_1_CREATE_DEVICE_CONTEXT_STATE_FLAG (d3d11_1.h)
author: windows-sdk-content
description: Describes flags that are used to create a device context state object (ID3DDeviceContextState) with the ID3D11Device1::CreateDeviceContextState method.
old-location: direct3d11\d3d11_1_create_device_context_state_flag.htm
tech.root: direct3d11
ms.assetid: 45F1C268-AA8A-44D5-BE9E-0C185738EB69
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D11_1_CREATE_DEVICE_CONTEXT_STATE_FLAG, D3D11_1_CREATE_DEVICE_CONTEXT_STATE_FLAG enumeration [Direct3D 11], D3D11_1_CREATE_DEVICE_CONTEXT_STATE_SINGLETHREADED, d3d11_1/D3D11_1_CREATE_DEVICE_CONTEXT_STATE_FLAG, d3d11_1/D3D11_1_CREATE_DEVICE_CONTEXT_STATE_SINGLETHREADED, direct3d11.d3d11_1_create_device_context_state_flag
ms.topic: enum
f1_keywords: ["d3d11_1/D3D11_1_CREATE_DEVICE_CONTEXT_STATE_FLAG"]
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11_1.h
api_name:
 - D3D11_1_CREATE_DEVICE_CONTEXT_STATE_FLAG
product: Windows
targetos: Windows
req.typenames: D3D11_1_CREATE_DEVICE_CONTEXT_STATE_FLAG
req.redist: 
ms.custom: 19H1
---

# D3D11_1_CREATE_DEVICE_CONTEXT_STATE_FLAG enumeration


## -description


Describes flags that are used to create a device context state object (<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate">ID3DDeviceContextState</a>) with the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11device1-createdevicecontextstate">ID3D11Device1::CreateDeviceContextState</a> method.


## -enum-fields




### -field D3D11_1_CREATE_DEVICE_CONTEXT_STATE_SINGLETHREADED

You use this flag if your application will only call methods of Direct3D 11 and Direct3D 10 interfaces from a single thread. By default, Direct3D 11 and Direct3D 10 are  <a href="https://docs.microsoft.com/windows/desktop/direct3d11/overviews-direct3d-11-render-multi-thread-differences">thread-safe</a>. 
        By using this flag, you can increase performance. However, if you use this flag and your application calls methods from multiple threads, undefined behavior might result.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-enums">Core Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11device1-createdevicecontextstate">ID3D11Device1::CreateDeviceContextState</a>
 

 

