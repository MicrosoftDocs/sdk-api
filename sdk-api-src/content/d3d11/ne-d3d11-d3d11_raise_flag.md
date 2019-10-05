---
UID: NE:d3d11.D3D11_RAISE_FLAG
title: D3D11_RAISE_FLAG (d3d11.h)
author: windows-sdk-content
description: Option(s) for raising an error to a non-continuable exception.
old-location: direct3d11\d3d11_raise_flag.htm
tech.root: direct3d11
ms.assetid: cdb88a12-153d-4f92-89c8-d3dab1b6bed5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 629223d9-c558-e5d3-12db-bfbc10b77ade, D3D11_RAISE_FLAG, D3D11_RAISE_FLAG enumeration [Direct3D 11], D3D11_RAISE_FLAG_DRIVER_INTERNAL_ERROR, d3d11/D3D11_RAISE_FLAG, d3d11/D3D11_RAISE_FLAG_DRIVER_INTERNAL_ERROR, direct3d11.d3d11_raise_flag
ms.topic: enum
f1_keywords: 
 - "d3d11/D3D11_RAISE_FLAG"
dev_langs:
 - c++
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
 - D3D11_RAISE_FLAG
targetos: Windows
req.typenames: D3D11_RAISE_FLAG
req.redist: 
ms.custom: 19H1
---

# D3D11_RAISE_FLAG enumeration


## -description


Option(s) for raising an error to a non-continuable exception.


## -enum-fields




### -field D3D11_RAISE_FLAG_DRIVER_INTERNAL_ERROR

Raise an internal driver error to a non-continuable exception.


## -remarks



These flags are used by <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11device-getexceptionmode">ID3D11Device::GetExceptionMode</a> and <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11device-setexceptionmode">ID3D11Device::SetExceptionMode</a>. Use 0 to indicate no flags; multiple flags can be logically OR'ed together.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-enums">Core Enumerations</a>
 

 

