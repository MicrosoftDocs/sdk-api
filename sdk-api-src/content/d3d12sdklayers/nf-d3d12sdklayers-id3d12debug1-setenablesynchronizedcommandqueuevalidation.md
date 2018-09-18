---
UID: NF:d3d12sdklayers.ID3D12Debug1.SetEnableSynchronizedCommandQueueValidation
title: ID3D12Debug1::SetEnableSynchronizedCommandQueueValidation
author: windows-sdk-content
description: Enables or disables dependent command queue synchronization when using a D3D12 device with the debug layer enabled.
old-location: direct3d12\id3d12debugdevice1_setenablesynchronizedcommandqueuevalidation.htm
tech.root: direct3d12
ms.assetid: B2038241-201B-402B-9B5A-BA2D2239A62A
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ID3D12Debug1 interface,SetEnableSynchronizedCommandQueueValidation method, ID3D12Debug1.SetEnableSynchronizedCommandQueueValidation, ID3D12Debug1::SetEnableSynchronizedCommandQueueValidation, SetEnableSynchronizedCommandQueueValidation, SetEnableSynchronizedCommandQueueValidation method, SetEnableSynchronizedCommandQueueValidation method,ID3D12Debug1 interface, d3d12sdklayers/ID3D12Debug1::SetEnableSynchronizedCommandQueueValidation, direct3d12.id3d12debugdevice1_setenablesynchronizedcommandqueuevalidation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d12sdklayers.h
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
 - COM
api_location:
 - d3d12sdklayers.h
api_name:
 - ID3D12Debug1.SetEnableSynchronizedCommandQueueValidation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12Debug1::SetEnableSynchronizedCommandQueueValidation


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Enables or disables dependent command queue synchronization when using a D3D12 device with the debug layer enabled.


## -parameters




### -param Enable

Type: <b>BOOL</b>

TRUE to enable Dependent Command Queue Synchronization, otherwise FALSE.


## -returns



This method does not return a value.




## -remarks



Dependent Command Queue Synchronization is a D3D12 Debug Layer feature that gives the debug layer the ability to track resource states more accurately when enabled.  Dependent Command Queue Synchronization is enabled by default.  

When Dependent Command Queue Synchronization is enabled, the debug layer holds back actual submission of GPU work until all outstanding fence <a href="https://msdn.microsoft.com/75D494D0-BCEC-453E-AB4F-E57CE2C9B318">Wait</a> conditions are met.  This gives the debug layer the ability to make reasonable assumptions about GPU state (such as resource states) on the CPU-timeline when multiple command queues are potentially doing concurrent work.

With Dependent Command Queue Synchronization disabled, all resource states tracked by the debug layer are cleared each time <a href="https://msdn.microsoft.com/487E2DED-C741-4376-9EE2-3DDD2F4F76BB">ID3D12CommandQueue::Signal</a> is called.  This results in significantly less useful resource state validation.

Disabling Dependent Command Queue Synchronization may reduce some debug layer performance overhead when using multiple command queues.  However, it is suggested to leave it enabled unless this overhead is problematic.  Note that applications that use only a single command queue will see no performance changes with Dependent Command Queue Synchronization disabled.




## -see-also




<a href="https://msdn.microsoft.com/3D69D0CA-5D45-49EA-BCF0-5B0ABB916261">ID3D12Debug1</a>
 

 

