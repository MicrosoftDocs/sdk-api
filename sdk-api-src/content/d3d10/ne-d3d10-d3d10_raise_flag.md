---
UID: NE:d3d10.D3D10_RAISE_FLAG
title: D3D10_RAISE_FLAG
author: windows-sdk-content
description: Option(s) for raising an error to a non-continuable exception.
old-location: direct3d10\d3d10_raise_flag.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_raise_flag.htm
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: 4f0a160b-254f-303d-968b-d35d73102d48, D3D10_RAISE_FLAG, D3D10_RAISE_FLAG enumeration [Direct3D 10], D3D10_RAISE_FLAG_DRIVER_INTERNAL_ERROR, d3d10/D3D10_RAISE_FLAG, d3d10/D3D10_RAISE_FLAG_DRIVER_INTERNAL_ERROR, direct3d10.d3d10_raise_flag
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3d10.h
req.include-header: 
req.redist: 
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
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_RAISE_FLAG
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



These flags are used by <a href="https://msdn.microsoft.com/en-us/library/Bb173572(v=VS.85).aspx">ID3D10Device::GetExceptionMode</a> and <a href="https://msdn.microsoft.com/en-us/library/Bb173614(v=VS.85).aspx">ID3D10Device::SetExceptionMode</a>. Use 0 to indicate no flags; multiple flags can be logically OR'ed together.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205150(v=VS.85).aspx">Core Enumerations</a>
 

 

