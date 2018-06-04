---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# D3D11_CLEAR_FLAG enumeration


## -description



      Specifies the parts of the depth stencil to clear.


## -enum-fields




### -field D3D11_CLEAR_DEPTH

Clear the depth buffer, using fast clear if possible, then place the resource in a compressed state.


### -field D3D11_CLEAR_STENCIL

Clear the stencil buffer, using fast clear if possible, then place the resource in a compressed state.


## -remarks




          These flags are used when calling <a href="https://msdn.microsoft.com/1e2269cf-edef-466e-be59-95dc644c7a0c">ID3D11DeviceContext::ClearDepthStencilView</a>; the flags can be combined with a bitwise OR.
        




## -see-also




<a href="https://msdn.microsoft.com/1641713a-5ac8-4597-900b-1bba54f9f522">Core Enumerations</a>
 

 

