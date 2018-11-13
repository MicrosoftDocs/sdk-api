---
UID: NF:d3d12.ID3D12GraphicsCommandList.BeginEvent
title: ID3D12GraphicsCommandList::BeginEvent
author: windows-sdk-content
description: Not intended to be called directly.  Use the PIX event runtime to insert events into a command list.
old-location: direct3d12\id3d12graphicscommandlist_beginevent.htm
tech.root: direct3d12
ms.assetid: 2A5292C0-ED9B-4E3C-87E4-88EA2FF09B28
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: BeginEvent, BeginEvent method, BeginEvent method,ID3D12GraphicsCommandList interface, ID3D12GraphicsCommandList interface,BeginEvent method, ID3D12GraphicsCommandList.BeginEvent, ID3D12GraphicsCommandList::BeginEvent, d3d12/ID3D12GraphicsCommandList::BeginEvent, direct3d12.id3d12graphicscommandlist_beginevent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12GraphicsCommandList.BeginEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12GraphicsCommandList::BeginEvent


## -description


Not intended to be called directly.  Use the
        <a href="https://blogs.msdn.microsoft.com/pix/winpixeventruntime/">PIX event runtime</a> to insert events into a command list.


## -parameters




### -param Metadata

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Internal.
          


### -param pData [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">void</a>*</b>

Internal.
          


### -param Size

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Internal.

          


## -returns



This method does not return a value.
          




## -remarks



This is a support method used internally by the PIX event runtime.  It is not intended to be called directly.

To mark the start of an instrumentation region at the current location within a D3D12 command list, use the <b>PIXBeginEvent</b> function or <b>PIXScopedEvent</b> macro.  These are provided by the <a href="https://blogs.msdn.microsoft.com/pix/winpixeventruntime/">WinPixEventRuntime</a> NuGet package.




## -see-also




<a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a>
 

 

