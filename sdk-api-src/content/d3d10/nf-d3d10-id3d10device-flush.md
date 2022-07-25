---
UID: NF:d3d10.ID3D10Device.Flush
title: ID3D10Device::Flush (d3d10.h)
description: Send queued-up commands in the command buffer to the GPU.
helpviewer_keywords: ["95043c81-fb9f-c3b0-6f27-f9c309dbec57","Flush","Flush method [Direct3D 10]","Flush method [Direct3D 10]","ID3D10Device interface","ID3D10Device interface [Direct3D 10]","Flush method","ID3D10Device.Flush","ID3D10Device::Flush","d3d10/ID3D10Device::Flush","direct3d10.id3d10device_flush"]
old-location: direct3d10\id3d10device_flush.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_flush.htm
ms.date: 12/05/2018
ms.keywords: 95043c81-fb9f-c3b0-6f27-f9c309dbec57, Flush, Flush method [Direct3D 10], Flush method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],Flush method, ID3D10Device.Flush, ID3D10Device::Flush, d3d10/ID3D10Device::Flush, direct3d10.id3d10device_flush
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Device::Flush
 - d3d10/ID3D10Device::Flush
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.Flush
---

# ID3D10Device::Flush


## -description

Send queued-up commands in the command buffer to the GPU.



## -remarks

Most applications will not need to call this method. Calling this method when not necessary will incur a performance penalty. Each call to <b>Flush</b> incurs a significant amount of overhead.

When Direct3D state-setting, present, or draw commands are called by an application, those commands are queued into an internal command buffer. <b>Flush</b> sends those commands to the GPU for processing. Normally, these commands are sent to the GPU automatically whenever Direct3D determines that they need to be, such as when the command buffer is full or when mapping a resource. <b>Flush</b> will send the commands manually.

<b>Flush</b> should be used when the CPU waits for an arbitrary amount of time (such as when calling <a href="/windows/desktop/api/synchapi/nf-synchapi-sleep">Sleep</a>, <a href="/windows/desktop/direct3d10/id3dx10threadpump-waitforallitems">ID3DX10ThreadPump::WaitForAllItems</a>, or <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-waitforvblank">WaitForVBlank</a>.

For more information about how flushing works, see <a href="/windows/desktop/direct3d9/accurately-profiling-direct3d-api-calls">Accurately Profiling Direct3D API Calls (Direct3D 9)</a>.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
