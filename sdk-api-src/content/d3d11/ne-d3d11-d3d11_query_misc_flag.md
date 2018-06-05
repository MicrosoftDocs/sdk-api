---
UID: NE:d3d11.D3D11_QUERY_MISC_FLAG
title: D3D11_QUERY_MISC_FLAG
author: windows-sdk-content
description: Flags that describe miscellaneous query behavior.
old-location: direct3d11\d3d11_query_misc_flag.htm
old-project: direct3d11
ms.assetid: a49a04f9-5804-43fb-b12d-f703721f4d30
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: D3D11_QUERY_MISC_FLAG, D3D11_QUERY_MISC_FLAG enumeration [Direct3D 11], D3D11_QUERY_MISC_PREDICATEHINT, d3d11/D3D11_QUERY_MISC_FLAG, d3d11/D3D11_QUERY_MISC_PREDICATEHINT, direct3d11.d3d11_query_misc_flag, f27525ae-a29c-15ac-7fd8-0d7cafc87209
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D11_QUERY_MISC_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D11.h
api_name:
-	D3D11_QUERY_MISC_FLAG
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_QUERY_MISC_FLAG enumeration


## -description


Flags that describe miscellaneous query behavior.


## -enum-fields




### -field D3D11_QUERY_MISC_PREDICATEHINT

Tell the hardware that if it is not yet sure if something is hidden or not to draw it anyway. This is only used with an occlusion predicate. Predication data cannot be returned to your application via <a href="https://msdn.microsoft.com/338d02ad-2227-49e5-9b4f-fb86a3898f73">ID3D11DeviceContext::GetData</a> when using this flag.


## -remarks



This flag is part of a query description (see <a href="https://msdn.microsoft.com/2ed8e380-744b-41e1-87c8-9c7e8100ea2f">D3D11_QUERY_DESC</a>).




## -see-also




<a href="https://msdn.microsoft.com/1641713a-5ac8-4597-900b-1bba54f9f522">Core Enumerations</a>
 

 

