---
UID: NS:d3d10sdklayers.D3D10_INFO_QUEUE_FILTER
title: D3D10_INFO_QUEUE_FILTER
author: windows-driver-content
description: Debug message filter; contains a lists of message types to allow or deny.
old-location: direct3d10\d3d10_info_queue_filter.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_info_queue_filter.htm
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: 9c94d10b-2b6f-b70e-75d1-72a61687e2b9, D3D10_INFO_QUEUE_FILTER, D3D10_INFO_QUEUE_FILTER structure [Direct3D 10], d3d10sdklayers/D3D10_INFO_QUEUE_FILTER, direct3d10.d3d10_info_queue_filter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d10sdklayers.h
req.include-header: D3D10.h
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
req.typenames: D3D10_INFO_QUEUE_FILTER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d10sdklayers.h
api_name:
-	D3D10_INFO_QUEUE_FILTER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D10_INFO_QUEUE_FILTER structure


## -description


Debug message filter; contains a lists of message types to allow or deny.


## -struct-fields




### -field AllowList

Type: <b><a href="https://msdn.microsoft.com/574cb8e3-4923-4731-b99d-680749fffbae">D3D10_INFO_QUEUE_FILTER_DESC</a></b>

A <a href="https://msdn.microsoft.com/574cb8e3-4923-4731-b99d-680749fffbae">D3D10_INFO_QUEUE_FILTER_DESC</a> structure describing the types of messages the info queue should allow.


### -field DenyList

Type: <b><a href="https://msdn.microsoft.com/574cb8e3-4923-4731-b99d-680749fffbae">D3D10_INFO_QUEUE_FILTER_DESC</a></b>

A <a href="https://msdn.microsoft.com/574cb8e3-4923-4731-b99d-680749fffbae">D3D10_INFO_QUEUE_FILTER_DESC</a> structure describing the types of messages the info queue should reject.


## -remarks



For use with an <a href="https://msdn.microsoft.com/b1405273-53f4-49da-acf5-832e73a25ac2">ID3D10InfoQueue Interface</a>.

Providing an allow list with non-zero values causes only the specified combination of categories, severities and message IDs to be allowed.  
      Messages that do not match the specified combination will be rejected.

Providing a deny list with non-zero values causes the specified combination of categories, severities and message IDs to be rejected.
      Messages that do not match the specified combination will be allowed.




## -see-also




<a href="https://msdn.microsoft.com/84769515-3f3b-4464-9620-7b806bf905b3">Core Structures</a>
 

 

