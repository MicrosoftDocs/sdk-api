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

# D3D12_DISCARD_REGION structure


## -description



          Describes details for the discard-resource operation.
        


## -struct-fields




### -field NumRects


            The number of rectangles in the array that the <b>pRects</b> member specifies.
          


### -field pRects


            An array of <b>D3D12_RECT</b> structures for the rectangles in the resource to discard.
            If <b>NULL</b>, <a href="https://msdn.microsoft.com/2F4DBA5B-F586-4126-8867-BEE650F6D161">DiscardResource</a> discards the entire resource.
          


### -field FirstSubresource


            Index of the first subresource in the resource to discard.
          


### -field NumSubresources


            The number of subresources in the resource to discard.
          


## -remarks




        This structure is used by the <a href="https://msdn.microsoft.com/2F4DBA5B-F586-4126-8867-BEE650F6D161">ID3D12GraphicsCommandList::DiscardResource</a> method.
      


        If rectangles are supplied in this structure, the resource must have 2D subresources with all specified subresources the same dimension.
      




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

