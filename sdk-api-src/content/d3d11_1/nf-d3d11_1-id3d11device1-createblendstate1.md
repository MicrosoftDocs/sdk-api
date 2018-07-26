---
UID: NF:d3d11_1.ID3D11Device1.CreateBlendState1
title: ID3D11Device1::CreateBlendState1
author: windows-sdk-content
description: Creates a blend-state object that encapsulates blend state for the output-merger stage and allows the configuration of logic operations.
old-location: direct3d11\id3d11device1_createblendstate1.htm
old-project: direct3d11
ms.assetid: 2E891104-3706-46A5-88FB-C621C95B4EFB
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: CreateBlendState1, CreateBlendState1 method [Direct3D 11], CreateBlendState1 method [Direct3D 11],ID3D11Device1 interface, ID3D11Device1 interface [Direct3D 11],CreateBlendState1 method, ID3D11Device1.CreateBlendState1, ID3D11Device1::CreateBlendState1, d3d11_1/ID3D11Device1::CreateBlendState1, direct3d11.id3d11device1_createblendstate1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11_1.h
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
tech.root: 
req.typenames: D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Device1.CreateBlendState1
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11Device1::CreateBlendState1


## -description


Creates a blend-state object that encapsulates blend state for the <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">output-merger stage</a> and allows the configuration of logic operations.


## -parameters




### -param pBlendStateDesc [in]

A pointer to a  <a href="https://msdn.microsoft.com/BBBECB86-B33D-4AA3-8D0A-45AEC3BBC4AB">D3D11_BLEND_DESC1</a> structure that describes blend state.


### -param ppBlendState [out, optional]

Address of a pointer to the <a href="https://msdn.microsoft.com/5562F0B2-77FC-4614-BFA9-077323D4A2FA">ID3D11BlendState1</a> interface for the blend-state object created.


## -returns



This method returns E_OUTOFMEMORY if there is insufficient memory to create the blend-state object.  
        See <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a> for other possible return values.




## -remarks



The logical operations (those that enable bitwise logical operations between pixel shader output and render target contents, refer to <a href="https://msdn.microsoft.com/A8323E69-F385-4E91-8B1F-A7CD3D508A09">D3D11_RENDER_TARGET_BLEND_DESC1</a> ) are only available on certain feature levels; call <a href="https://msdn.microsoft.com/7edf2ffd-908a-4cf8-9ac6-8fd14d7a0ea1">CheckFeatureSupport</a> with D3D11_FEATURE_D3D11_OPTIONS set, to ensure support by checking the boolean field  <i>OutputMergerLogicOp</i> of <a href="https://msdn.microsoft.com/02A3B423-75AB-4F44-BEBE-B8039EF384DC">D3D11_FEATURE_DATA_D3D11_OPTIONS</a>.

An app can create up to 4096 unique blend-state objects. For each object created, the runtime checks to see if a previous object 
      has the same state. If such a previous object exists, the runtime will return a pointer to previous instance instead of creating a duplicate object.




## -see-also




<a href="https://msdn.microsoft.com/DB4DAD13-3CD7-4362-950B-6403328CB071">ID3D11Device1</a>
 

 

