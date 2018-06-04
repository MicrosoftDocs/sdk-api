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

# D3D12_VIEWPORT structure


## -description


Describes the dimensions of a viewport.


## -struct-fields




### -field TopLeftX

X position of the left hand side of the viewport. 


### -field TopLeftY

Y position of the top of the viewport. 


### -field Width

Width of the viewport.


### -field Height

Height of the viewport.


### -field MinDepth

Minimum depth of the viewport. Ranges between 0 and 1.


### -field MaxDepth

Maximum depth of the viewport. Ranges between 0 and 1.


## -remarks



Pass an array of these structures to the <i>pViewports</i> parameter  in a call to  <a href="https://msdn.microsoft.com/1ACFD260-1CE5-484C-83DD-021E8D895EBB">ID3D12GraphicsCommandList::RSSetViewports</a> to set viewports for the display.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

