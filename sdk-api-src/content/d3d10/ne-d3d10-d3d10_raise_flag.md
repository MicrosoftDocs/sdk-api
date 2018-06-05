---
UID: NE:d3d10.D3D10_RAISE_FLAG
title: D3D10_RAISE_FLAG
author: windows-sdk-content
description: Option(s) for raising an error to a non-continuable exception.
old-location: direct3d10\d3d10_raise_flag.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_raise_flag.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: 4f0a160b-254f-303d-968b-d35d73102d48, D3D10_RAISE_FLAG, D3D10_RAISE_FLAG enumeration [Direct3D 10], D3D10_RAISE_FLAG_DRIVER_INTERNAL_ERROR, d3d10/D3D10_RAISE_FLAG, d3d10/D3D10_RAISE_FLAG_DRIVER_INTERNAL_ERROR, direct3d10.d3d10_raise_flag
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3d10.h
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
req.typenames: D3D10_RAISE_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D10.h
api_name:
-	D3D10_RAISE_FLAG
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# D3D10_RAISE_FLAG enumeration


## -description


Option(s) for raising an error to a non-continuable exception.


## -enum-fields




### -field D3D10_RAISE_FLAG_DRIVER_INTERNAL_ERROR

Raise an internal driver error to a non-continuable exception.


## -remarks



These flags are used by <a href="https://msdn.microsoft.com/c343ba41-4fec-4598-8eac-30674ab77a49">ID3D10Device::GetExceptionMode</a> and <a href="https://msdn.microsoft.com/bd15256d-4dc8-43d5-87de-2d35956dc0bd">ID3D10Device::SetExceptionMode</a>. Use 0 to indicate no flags; multiple flags can be logically OR'ed together.




## -see-also




<a href="https://msdn.microsoft.com/3d1541bf-75d8-459d-a912-4068e9a0a9e4">Core Enumerations</a>
 

 

