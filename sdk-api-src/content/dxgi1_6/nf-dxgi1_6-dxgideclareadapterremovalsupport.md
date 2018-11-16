---
UID: NF:dxgi1_6.DXGIDeclareAdapterRemovalSupport
title: DXGIDeclareAdapterRemovalSupport function
author: windows-sdk-content
description: Allows a process to indicate that it's resilient to any of its graphics devices being removed.
old-location: direct3ddxgi\dxgideclareadapterremovalsupport.htm
tech.root: direct3ddxgi
ms.assetid: 602EA66C-6D3D-4604-822C-DBD66EB70C3C
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DXGIDeclareAdapterRemovalSupport, DXGIDeclareAdapterRemovalSupport function [DXGI], direct3ddxgi.dxgideclareadapterremovalsupport, dxgi1_6/DXGIDeclareAdapterRemovalSupport
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dxgi1_6.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: Dxgi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - dxgi.dll
api_name:
 - DXGIDeclareAdapterRemovalSupport
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- DXGIDeclareAdapterRemovalSupport
: 
---

# DXGIDeclareAdapterRemovalSupport function


## -description


Allows a process to indicate that it's resilient to any of its graphics devices being removed.


## -parameters






## -returns



Type: <b>HRESULT</b>

Returns <b>S_OK</b> if successful; an error code otherwise. If this function is called after device creation, it returns <b>DXGI_ERROR_INVALID_CALL</b>. If this is not the first time that this function is called, it returns <b>DXGI_ERROR_ALREADY_EXISTS</b>. For a full list of error codes, see <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>.




## -remarks



This function is graphics API-agonistic, meaning that apps running on other APIs, such as OpenGL and Vulkan, would also apply.

This function should be called once per process and before any device creation.




## -see-also




<a href="https://github.com/Microsoft/DirectX-Graphics-Samples/tree/develop/Tools/DXGIAdapterRemovalSupportTest">DXGI AdapterRemovalSupport test sample</a>



<a href="https://msdn.microsoft.com/209d2e65-b118-47a7-aece-fb140fdede3f">DXGI Functions</a>



<a href="https://github.com/Microsoft/DirectX-Graphics-Samples/tree/develop/Samples/UWP/D3D12xGPU">xGPU UWP sample</a>



<a href="https://github.com/Microsoft/DirectX-Graphics-Samples/tree/develop/Samples/Desktop/D3D12xGPU">xGPU desktop sample</a>
 

 

