---
UID: NS:d3d11.D3D11_COUNTER_DESC
title: D3D11_COUNTER_DESC (d3d11.h)
author: windows-sdk-content
description: Describes a counter.
old-location: direct3d11\d3d11_counter_desc.htm
tech.root: direct3d11
ms.assetid: a0816409-fbe1-4b45-9b69-6f85b20008cb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 37ab8337-bf1a-9bbe-268c-5a6aa3f34dda, D3D11_COUNTER_DESC, D3D11_COUNTER_DESC structure [Direct3D 11], d3d11/D3D11_COUNTER_DESC, direct3d11.d3d11_counter_desc
ms.topic: struct
f1_keywords: ["d3d11/D3D11_COUNTER_DESC"]
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: D3D11_COUNTER_DESC
req.redist: 
ms.custom: 19H1
---

# D3D11_COUNTER_DESC structure


## -description


Describes a counter.


## -struct-fields




### -field Counter

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d11/ne-d3d11-d3d11_counter">D3D11_COUNTER</a></b>

Type of counter (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/ne-d3d11-d3d11_counter">D3D11_COUNTER</a>).


### -field MiscFlags

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Reserved.


## -remarks



This structure is used by <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11counter-getdesc">ID3D11Counter::GetDesc</a>, <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkcounter">ID3D11Device::CheckCounter</a> and <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createcounter">ID3D11Device::CreateCounter</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-structures">Core Structures</a>
 

 

