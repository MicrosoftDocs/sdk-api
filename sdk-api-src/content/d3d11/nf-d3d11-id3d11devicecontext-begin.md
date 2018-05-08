---
UID: NF:d3d11.ID3D11DeviceContext.Begin
title: ID3D11DeviceContext::Begin
author: windows-driver-content
description: Mark the beginning of a series of commands.
old-location: direct3d11\id3d11devicecontext_begin.htm
old-project: direct3d11
ms.assetid: 5a9cdc60-2226-4d18-bfbd-5db10de35e53
ms.author: windowsdriverdev
ms.date: 4/6/2018
ms.keywords: Begin, Begin method [Direct3D 11], Begin method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],Begin method, ID3D11DeviceContext.Begin, ID3D11DeviceContext::Begin, d3d11/ID3D11DeviceContext::Begin, direct3d11.id3d11devicecontext_begin, e0186f02-1f56-8ba4-2429-48dc47ff8dc9
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11.h
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
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D11.lib
-	D3D11.dll
api_name:
-	ID3D11DeviceContext.Begin
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11DeviceContext::Begin


## -description


Mark the beginning of a series of commands.


## -parameters




### -param pAsync [in]

Type: <b><a href="https://msdn.microsoft.com/37ff9dc0-5ec2-4cd5-b252-44e2dac45355">ID3D11Asynchronous</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/37ff9dc0-5ec2-4cd5-b252-44e2dac45355">ID3D11Asynchronous</a> interface.


## -returns



Returns nothing.




## -remarks



Use <a href="https://msdn.microsoft.com/9b941abc-04a3-4dd7-b72d-62cd5bd06b47">ID3D11DeviceContext::End</a> to mark the ending of the series of commands.




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

