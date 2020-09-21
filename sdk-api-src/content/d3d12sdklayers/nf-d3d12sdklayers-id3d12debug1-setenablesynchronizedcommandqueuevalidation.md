---
UID: NF:d3d12sdklayers.ID3D12Debug1.SetEnableSynchronizedCommandQueueValidation
title: ID3D12Debug1::SetEnableSynchronizedCommandQueueValidation (d3d12sdklayers.h)
description: Enables or disables dependent command queue synchronization when using a D3D12 device with the debug layer enabled.
helpviewer_keywords: ["ID3D12Debug1 interface","SetEnableSynchronizedCommandQueueValidation method","ID3D12Debug1.SetEnableSynchronizedCommandQueueValidation","ID3D12Debug1::SetEnableSynchronizedCommandQueueValidation","SetEnableSynchronizedCommandQueueValidation","SetEnableSynchronizedCommandQueueValidation method","SetEnableSynchronizedCommandQueueValidation method","ID3D12Debug1 interface","d3d12sdklayers/ID3D12Debug1::SetEnableSynchronizedCommandQueueValidation","direct3d12.id3d12debugdevice1_setenablesynchronizedcommandqueuevalidation"]
old-location: direct3d12\id3d12debugdevice1_setenablesynchronizedcommandqueuevalidation.htm
tech.root: direct3d12
ms.assetid: B2038241-201B-402B-9B5A-BA2D2239A62A
ms.date: 12/05/2018
ms.keywords: ID3D12Debug1 interface,SetEnableSynchronizedCommandQueueValidation method, ID3D12Debug1.SetEnableSynchronizedCommandQueueValidation, ID3D12Debug1::SetEnableSynchronizedCommandQueueValidation, SetEnableSynchronizedCommandQueueValidation, SetEnableSynchronizedCommandQueueValidation method, SetEnableSynchronizedCommandQueueValidation method,ID3D12Debug1 interface, d3d12sdklayers/ID3D12Debug1::SetEnableSynchronizedCommandQueueValidation, direct3d12.id3d12debugdevice1_setenablesynchronizedcommandqueuevalidation
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12Debug1::SetEnableSynchronizedCommandQueueValidation
 - d3d12sdklayers/ID3D12Debug1::SetEnableSynchronizedCommandQueueValidation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12sdklayers.h
api_name:
 - ID3D12Debug1.SetEnableSynchronizedCommandQueueValidation
---

# ID3D12Debug1::SetEnableSynchronizedCommandQueueValidation


## -description

Enables or disables dependent command queue synchronization when using a D3D12 device with the debug layer enabled.

## -parameters

### -param Enable

Type: <b>BOOL</b>

TRUE to enable Dependent Command Queue Synchronization, otherwise FALSE.

## -remarks

Dependent Command Queue Synchronization is a D3D12 Debug Layer feature that gives the debug layer the ability to track resource states more accurately when enabled.  Dependent Command Queue Synchronization is enabled by default.  

When Dependent Command Queue Synchronization is enabled, the debug layer holds back actual submission of GPU work until all outstanding fence <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-wait">Wait</a> conditions are met.  This gives the debug layer the ability to make reasonable assumptions about GPU state (such as resource states) on the CPU-timeline when multiple command queues are potentially doing concurrent work.

With Dependent Command Queue Synchronization disabled, all resource states tracked by the debug layer are cleared each time <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-signal">ID3D12CommandQueue::Signal</a> is called.  This results in significantly less useful resource state validation.

Disabling Dependent Command Queue Synchronization may reduce some debug layer performance overhead when using multiple command queues.  However, it is suggested to leave it enabled unless this overhead is problematic.  Note that applications that use only a single command queue will see no performance changes with Dependent Command Queue Synchronization disabled.

## -see-also

<a href="/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1">ID3D12Debug1</a>