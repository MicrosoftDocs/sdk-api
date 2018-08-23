---
UID: NF:dxgi1_3.IDXGIFactory3.GetCreationFlags
title: IDXGIFactory3::GetCreationFlags
author: windows-sdk-content
description: Gets the flags that were used when a Microsoft DirectX Graphics Infrastructure (DXGI) object was created.
old-location: direct3ddxgi\idxgifactory3_getcreationflags.htm
old-project: direct3ddxgi
ms.assetid: 1B4A5DC9-6853-4047-B64D-BD251352AC89
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: GetCreationFlags, GetCreationFlags method [DXGI], GetCreationFlags method [DXGI],IDXGIFactory3 interface, IDXGIFactory3 interface [DXGI],GetCreationFlags method, IDXGIFactory3.GetCreationFlags, IDXGIFactory3::GetCreationFlags, direct3ddxgi.idxgifactory3_getcreationflags, dxgi1_3/IDXGIFactory3::GetCreationFlags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dxgi1_3.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: DXGI_OVERLAY_SUPPORT_FLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxgi1_3.h
api_name:
 - IDXGIFactory3.GetCreationFlags
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIFactory3::GetCreationFlags


## -description


Gets the flags that were used when a Microsoft DirectX Graphics Infrastructure (DXGI) object was created.


## -parameters






## -returns



The creation flags.




## -remarks



The <b>GetCreationFlags</b> method returns flags that were passed to the  <a href="https://msdn.microsoft.com/D3CF43B0-8F17-486E-8750-CF0B9052BE74">CreateDXGIFactory2</a> function, or were implicitly constructed by <a href="https://msdn.microsoft.com/en-us/library/Bb204862(v=VS.85).aspx">CreateDXGIFactory</a>, <a href="https://msdn.microsoft.com/6fb9d7a3-0b59-4b7a-8871-b99d59811d46">CreateDXGIFactory1</a>,  <a href="https://msdn.microsoft.com/d1c85ec0-84a8-41ff-9cbe-f47bbaa5863b">D3D11CreateDevice</a>, or <a href="https://msdn.microsoft.com/84d73e8c-f13c-4343-91de-57f9f8a0ad96">D3D11CreateDeviceAndSwapChain</a>.




## -see-also




<a href="https://msdn.microsoft.com/63B7A8E3-9A8F-409F-84DA-E9303C52A146">IDXGIFactory3</a>
 

 

