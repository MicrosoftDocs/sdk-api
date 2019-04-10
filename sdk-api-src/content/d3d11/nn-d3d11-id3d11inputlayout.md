---
UID: NN:d3d11.ID3D11InputLayout
title: ID3D11InputLayout (d3d11.h)
author: windows-sdk-content
description: An input-layout interface holds a definition of how to feed vertex data that is laid out in memory into the input-assembler stage of the graphics pipeline.
old-location: direct3d11\id3d11inputlayout.htm
tech.root: direct3d11
ms.assetid: df83fcdc-ff1b-4901-9f1f-15eb2fe5241c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D11InputLayout, ID3D11InputLayout interface [Direct3D 11], ID3D11InputLayout interface [Direct3D 11],described, b8a9a875-1563-0aed-8b68-020a489fb28a, d3d11/ID3D11InputLayout, direct3d11.id3d11inputlayout
ms.topic: interface
req.header: d3d11.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11InputLayout
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11InputLayout interface


## -description


An input-layout interface holds a definition of how to feed vertex data that is laid out in memory into the <a href="https://msdn.microsoft.com/en-us/library/Bb205116(v=VS.85).aspx">input-assembler stage</a> of the <a href="https://msdn.microsoft.com/8e7a6f64-0a2b-4ea5-a6a6-7bfb87e27dcc">graphics pipeline</a>.


## -remarks



To create an input-layout object, call <a href="https://msdn.microsoft.com/fe233b7b-3729-428a-8611-e98ea4c5af35">ID3D11Device::CreateInputLayout</a>. To bind the input-layout object to the <a href="https://msdn.microsoft.com/en-us/library/Bb205116(v=VS.85).aspx">input-assembler stage</a>, call <a href="https://msdn.microsoft.com/54562ece-db8d-4e31-bde2-36391792e259">ID3D11DeviceContext::IASetInputLayout</a>.




## -see-also




<a href="https://msdn.microsoft.com/e96804db-0987-49ca-b1b1-321f36c13024">Core Interfaces</a>



<a href="https://msdn.microsoft.com/bed17239-0358-4768-8655-9a1d92f25a2e">ID3D11DeviceChild</a>
 

 

