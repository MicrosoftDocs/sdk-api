---
UID: NS:d3d11.D3D11_COUNTER_DESC
title: D3D11_COUNTER_DESC
author: windows-sdk-content
description: Describes a counter.
old-location: direct3d11\d3d11_counter_desc.htm
old-project: direct3d11
ms.assetid: a0816409-fbe1-4b45-9b69-6f85b20008cb
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: 37ab8337-bf1a-9bbe-268c-5a6aa3f34dda, D3D11_COUNTER_DESC, D3D11_COUNTER_DESC structure [Direct3D 11], d3d11/D3D11_COUNTER_DESC, direct3d11.d3d11_counter_desc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: D3D11_COUNTER_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_COUNTER_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_COUNTER_DESC structure


## -description


Describes a counter.


## -struct-fields




### -field Counter

Type: <b><a href="https://msdn.microsoft.com/b6a5cc7e-48e5-478a-aa9c-8b2878c0de6b">D3D11_COUNTER</a></b>

Type of counter (see <a href="https://msdn.microsoft.com/b6a5cc7e-48e5-478a-aa9c-8b2878c0de6b">D3D11_COUNTER</a>).


### -field MiscFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Reserved.


## -remarks



This structure is used by <a href="https://msdn.microsoft.com/2422b2d3-29c1-40cf-a41a-f9f299c2d436">ID3D11Counter::GetDesc</a>, <a href="https://msdn.microsoft.com/b09feac6-79c8-4f40-bfa1-028d4490b039">ID3D11Device::CheckCounter</a> and <a href="https://msdn.microsoft.com/857111cc-f590-4383-994c-a72402f8a4aa">ID3D11Device::CreateCounter</a>.




## -see-also




<a href="https://msdn.microsoft.com/2a45182a-7114-4075-b8b8-147f52fe7aa9">Core Structures</a>
 

 

