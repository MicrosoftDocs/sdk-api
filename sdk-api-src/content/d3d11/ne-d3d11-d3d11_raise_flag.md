---
UID: NE:d3d11.D3D11_RAISE_FLAG
title: D3D11_RAISE_FLAG
author: windows-driver-content
description: Option(s) for raising an error to a non-continuable exception.
old-location: direct3d11\d3d11_raise_flag.htm
old-project: direct3d11
ms.assetid: cdb88a12-153d-4f92-89c8-d3dab1b6bed5
ms.author: windowsdriverdev
ms.date: 4/6/2018
ms.keywords: 629223d9-c558-e5d3-12db-bfbc10b77ade, D3D11_RAISE_FLAG, D3D11_RAISE_FLAG enumeration [Direct3D 11], D3D11_RAISE_FLAG_DRIVER_INTERNAL_ERROR, d3d11/D3D11_RAISE_FLAG, d3d11/D3D11_RAISE_FLAG_DRIVER_INTERNAL_ERROR, direct3d11.d3d11_raise_flag
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: D3D11_RAISE_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D11.h
api_name:
-	D3D11_RAISE_FLAG
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_RAISE_FLAG enumeration


## -description


Option(s) for raising an error to a non-continuable exception.


## -enum-fields




### -field D3D11_RAISE_FLAG_DRIVER_INTERNAL_ERROR

Raise an internal driver error to a non-continuable exception.


## -remarks



These flags are used by <a href="https://msdn.microsoft.com/c5deddde-4355-4a34-b40a-50006029d590">ID3D11Device::GetExceptionMode</a> and <a href="https://msdn.microsoft.com/a442a5dc-7931-4464-a6e7-76441e61da5b">ID3D11Device::SetExceptionMode</a>. Use 0 to indicate no flags; multiple flags can be logically OR'ed together.




## -see-also




<a href="https://msdn.microsoft.com/1641713a-5ac8-4597-900b-1bba54f9f522">Core Enumerations</a>
 

 

