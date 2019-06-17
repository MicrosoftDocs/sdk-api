---
UID: NF:dxgi1_5.IDXGIFactory5.CheckFeatureSupport
title: IDXGIFactory5::CheckFeatureSupport (dxgi1_5.h)
author: windows-sdk-content
description: Used to check for hardware feature support.
old-location: direct3ddxgi\idxgifactory5_checkfeaturesupport.htm
tech.root: direct3ddxgi
ms.assetid: 959F83F8-ADC6-4609-8F63-BEDDFC2EF088
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CheckFeatureSupport, CheckFeatureSupport method [DXGI], CheckFeatureSupport method [DXGI],IDXGIFactory5 interface, IDXGIFactory5 interface [DXGI],CheckFeatureSupport method, IDXGIFactory5.CheckFeatureSupport, IDXGIFactory5::CheckFeatureSupport, direct3ddxgi.idxgifactory5_checkfeaturesupport, dxgi1_5/IDXGIFactory5::CheckFeatureSupport
ms.topic: method
f1_keywords: ["dxgi1_5/IDXGIFactory5.CheckFeatureSupport"]
req.header: dxgi1_5.h
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
req.lib: Dxgi.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGIFactory5.CheckFeatureSupport
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGIFactory5::CheckFeatureSupport


## -description


Used to check for hardware feature support.


## -parameters




### -param Feature

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_feature">DXGI_FEATURE</a></b>

Specifies one member of  <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_feature">DXGI_FEATURE</a> to query support for.


### -param pFeatureSupportData [in, out]

Type: <b>void*</b>

Specifies a pointer to a buffer that will be filled with data that describes the feature support.


### -param FeatureSupportDataSize

Type: <b>UINT</b>

The size, in bytes, of <i>pFeatureSupportData</i>.


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -remarks



Refer to the description of <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag">DXGI_SWAP_CHAIN_FLAG_ALLOW_TEARING</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_5/nn-dxgi1_5-idxgifactory5">IDXGIFactory5</a>
 

 

