---
UID: NF:d3d12.ID3D12GraphicsCommandList.EndEvent
title: ID3D12GraphicsCommandList::EndEvent (d3d12.h)
description: Not intended to be called directly.  Use the PIX event runtime to insert events into a command list. (ID3D12GraphicsCommandList.EndEvent)
helpviewer_keywords: ["EndEvent","EndEvent method","EndEvent method","ID3D12GraphicsCommandList interface","ID3D12GraphicsCommandList interface","EndEvent method","ID3D12GraphicsCommandList.EndEvent","ID3D12GraphicsCommandList::EndEvent","d3d12/ID3D12GraphicsCommandList::EndEvent","direct3d12.id3d12graphicscommandlist_endevent"]
old-location: direct3d12\id3d12graphicscommandlist_endevent.htm
tech.root: direct3d12
ms.assetid: 24C40BE8-1080-4478-AB7C-D1FFCF6F5E3F
ms.date: 12/05/2018
ms.keywords: EndEvent, EndEvent method, EndEvent method,ID3D12GraphicsCommandList interface, ID3D12GraphicsCommandList interface,EndEvent method, ID3D12GraphicsCommandList.EndEvent, ID3D12GraphicsCommandList::EndEvent, d3d12/ID3D12GraphicsCommandList::EndEvent, direct3d12.id3d12graphicscommandlist_endevent
req.header: d3d12.h
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
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12GraphicsCommandList::EndEvent
 - d3d12/ID3D12GraphicsCommandList::EndEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12GraphicsCommandList.EndEvent
---

# ID3D12GraphicsCommandList::EndEvent


## -description

Not intended to be called directly.  Use the
        <a href="https://devblogs.microsoft.com/pix/winpixeventruntime/">PIX event runtime</a> to insert events into a command list.



## -remarks

This is a support method used internally by the PIX event runtime.  It is not intended to be called directly.

To mark the end of an instrumentation region at the current location within a D3D12 command list, use the <b>PIXEndEvent</b> function or <b>PIXScopedEvent</b> macro.  These are provided by the <a href="https://devblogs.microsoft.com/pix/winpixeventruntime/">WinPixEventRuntime</a> NuGet package.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist">ID3D12GraphicsCommandList</a>
