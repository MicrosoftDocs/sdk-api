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

# ID3D11DeviceContext2::TiledResourceBarrier


## -description


Specifies a data access ordering constraint between multiple tiled resources.  For more info about this constraint, see Remarks.


## -parameters




### -param pTiledResourceOrViewAccessBeforeBarrier [in, optional]

Type: <b><a href="https://msdn.microsoft.com/bed17239-0358-4768-8655-9a1d92f25a2e">ID3D11DeviceChild</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a> or <a href="https://msdn.microsoft.com/060973b4-bf7d-4be2-b087-85a5b1bca905">ID3D11View</a> for a resource that was created with the <a href="https://msdn.microsoft.com/2a324055-21b0-4dad-a8e0-781905329dc2">D3D11_RESOURCE_MISC_TILED</a> flag.  Access operations on this object must complete before the access operations on the object that <i>pTiledResourceOrViewAccessAfterBarrier</i> specifies.


### -param pTiledResourceOrViewAccessAfterBarrier [in, optional]

Type: <b><a href="https://msdn.microsoft.com/bed17239-0358-4768-8655-9a1d92f25a2e">ID3D11DeviceChild</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a> or <a href="https://msdn.microsoft.com/060973b4-bf7d-4be2-b087-85a5b1bca905">ID3D11View</a> for a resource that was created with the <a href="https://msdn.microsoft.com/2a324055-21b0-4dad-a8e0-781905329dc2">D3D11_RESOURCE_MISC_TILED</a> flag.  Access operations on this object must begin after the access operations on the object that <i>pTiledResourceOrViewAccessBeforeBarrier</i> specifies.


## -returns



Returns nothing




## -remarks



Apps can use tiled resources to reuse tiles in different resources. But, a device and driver might not be able to determine whether some memory in a tile pool that was just rendered to is now being used for reading.


For example, an app can render to some tiles in a tile pool with one tiled resource but then read from the same tiles by using a different tiled resource. These tiled-resource operations are different from using one resource and then just switching from writing with <a href="https://msdn.microsoft.com/3ae7c255-2403-493a-9fb9-fc9795f6d920">ID3D11RenderTargetView</a> to reading with <a href="https://msdn.microsoft.com/289555d8-2a6e-454f-86bc-48fb2c8ea345">ID3D11ShaderResourceView</a>. The runtime already tracks and handles these one resource operations using <b>ID3D11RenderTargetView</b> and <b>ID3D11ShaderResourceView</b>.


When an app transitions from accessing (reading or writing) some location in a tile pool with one resource to accessing the same memory (read or write) via another tiled resource (with mappings to the same memory), the app must call <b>TiledResourceBarrier</b> after the first use of the resource and before the second. The parameters are the <i>pTiledResourceOrViewAccessBeforeBarrier</i> for accesses before the barrier (via rendering, copying), and the <i>pTiledResourceOrViewAccessAfterBarrier</i> for accesses after the barrier by using the same tile pool memory. If the resources are identical, the app doesn't need to call <b>TiledResourceBarrier</b> because this kind of hazard is already tracked and handled.


The barrier call informs the driver that operations issued to the resource before the call must complete before any accesses that occur after the call via a different tiled resource that shares the same memory.


Either or both of the parameters (before or after the barrier) can be <b>NULL</b>. <b>NULL</b> before the barrier means all tiled resource accesses before the barrier must complete before the resource specified after the barrier can be referenced by the graphics processing unit (GPU). <b>NULL</b> after the barrier means that any tiled resources accessed after the barrier can only be executed by the GPU after accesses to the tiled resources before the barrier are finished. Both <b>NULL</b> means all previous tiled resource accesses are complete before any subsequent tiled resource access can proceed. 


An app can pass a view pointer, a resource, or <b>NULL</b> for each parameter. Views are allowed not only for convenience but also to allow the app to scope the barrier effect to a relevant portion of a resource.


For more info about tiled resources, see <a href="https://msdn.microsoft.com/03083460-192B-40CB-8EE1-76DF6D95F72B">Tiled resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/8B6B6F6E-9236-4DEE-A1BA-5FE45736DFAA">ID3D11DeviceContext2</a>
 

 

