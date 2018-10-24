---
UID: NE:d3d10.D3D10_QUERY_MISC_FLAG
title: D3D10_QUERY_MISC_FLAG
author: windows-sdk-content
description: Flags that describe miscellaneous query behavior.
old-location: direct3d10\d3d10_query_misc_flag.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_query_misc_flag.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: D3D10_QUERY_MISC_FLAG, D3D10_QUERY_MISC_FLAG enumeration [Direct3D 10], D3D10_QUERY_MISC_PREDICATEHINT, afca49a1-e15e-21f0-d3cc-592d3ba4b0cd, d3d10/D3D10_QUERY_MISC_FLAG, d3d10/D3D10_QUERY_MISC_PREDICATEHINT, direct3d10.d3d10_query_misc_flag
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_QUERY_MISC_FLAG
product: Windows
targetos: Windows
req.typenames: D3D10_QUERY_MISC_FLAG
req.redist: 
---

# D3D10_QUERY_MISC_FLAG enumeration


## -description


Flags that describe miscellaneous query behavior.


## -enum-fields




### -field D3D10_QUERY_MISC_PREDICATEHINT

Tell the hardware that if it is not yet sure if something is hidden or not to draw it anyway. This is only used with an occlusion predicate. Predication data cannot be returned to your application via <a href="https://msdn.microsoft.com/en-us/library/Bb173503(v=VS.85).aspx">ID3D10Asynchronous::GetData</a> when using this flag.


## -remarks



This flag is part of a query description (see <a href="https://msdn.microsoft.com/en-us/library/Bb172405(v=VS.85).aspx">D3D10_QUERY_DESC</a>).




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205150(v=VS.85).aspx">Core Enumerations</a>
 

 

