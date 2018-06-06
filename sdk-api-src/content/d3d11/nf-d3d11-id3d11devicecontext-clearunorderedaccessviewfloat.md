---
UID: NF:d3d11.ID3D11DeviceContext.ClearUnorderedAccessViewFloat
title: ID3D11DeviceContext::ClearUnorderedAccessViewFloat
author: windows-sdk-content
description: Clears an unordered access resource with a float value.
old-location: direct3d11\id3d11devicecontext_clearunorderedaccessviewfloat.htm
old-project: direct3d11
ms.assetid: c93d8638-c624-402a-8e14-c85aa7b69930
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: 2a51f18d-5ea4-ef19-5a3f-a879736bdf6a, ClearUnorderedAccessViewFloat, ClearUnorderedAccessViewFloat method [Direct3D 11], ClearUnorderedAccessViewFloat method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],ClearUnorderedAccessViewFloat method, ID3D11DeviceContext.ClearUnorderedAccessViewFloat, ID3D11DeviceContext::ClearUnorderedAccessViewFloat, d3d11/ID3D11DeviceContext::ClearUnorderedAccessViewFloat, direct3d11.id3d11devicecontext_clearunorderedaccessviewfloat
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.ClearUnorderedAccessViewFloat
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11DeviceContext::ClearUnorderedAccessViewFloat


## -description


Clears an <a href="https://msdn.microsoft.com/597cc12f-dd0e-4603-b670-3f584f25e192">unordered access</a> resource with a float value.


## -parameters




### -param pUnorderedAccessView [in]

Type: <b><a href="https://msdn.microsoft.com/9def4a7d-f145-4073-8d7d-bf3c7ac7a060">ID3D11UnorderedAccessView</a>*</b>

The <a href="https://msdn.microsoft.com/9def4a7d-f145-4073-8d7d-bf3c7ac7a060">ID3D11UnorderedAccessView</a> to clear.


### -param Values [in]

Type: <b>const FLOAT[4]</b>

Values to copy to corresponding channels, see remarks.


## -returns



Returns nothing.




## -remarks



This API works on FLOAT, UNORM, and SNORM unordered access views (UAVs), with format conversion from FLOAT to *NORM where appropriate. On other UAVs, the operation is invalid and the call will not reach the driver.




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

