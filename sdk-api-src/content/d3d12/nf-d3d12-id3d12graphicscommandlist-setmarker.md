---
UID: NF:d3d12.ID3D12GraphicsCommandList.SetMarker
title: ID3D12GraphicsCommandList::SetMarker
author: windows-sdk-content
description: Not intended to be called directly.  Use the PIX event runtime to insert events into a command list.
old-location: direct3d12\id3d12graphicscommandlist_setmarker.htm
old-project: direct3d12
ms.assetid: 521844B8-0EF8-4F09-ABCE-E8C96129F548
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: ID3D12GraphicsCommandList interface,SetMarker method, ID3D12GraphicsCommandList.SetMarker, ID3D12GraphicsCommandList::SetMarker, SetMarker, SetMarker method, SetMarker method,ID3D12GraphicsCommandList interface, d3d12/ID3D12GraphicsCommandList::SetMarker, direct3d12.id3d12graphicscommandlist_setmarker
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D_SHADER_MODEL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12GraphicsCommandList.SetMarker
product: Windows
targetos: Windows
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
---

# ID3D12GraphicsCommandList::SetMarker


## -description



          Not intended to be called directly.  Use the
        <a href="https://blogs.msdn.microsoft.com/pix/winpixeventruntime/">PIX event runtime</a> to insert events into a command list.


## -parameters




### -param Metadata

Type: <b>UINT</b>


            Internal.
          


### -param pData [in, optional]

Type: <b>const void*</b>

Internal.


### -param Size

Type: <b>UINT</b>


            Internal.


## -returns




            This method does not return a value.
          




## -remarks



This is a support method used internally by the PIX event runtime.  It is not intended to be called directly.

To insert instrumentation markers at the current location within a D3D12 command list, use the <b>PIXSetMarker</b> function.  This is provided by the <a href="https://blogs.msdn.microsoft.com/pix/winpixeventruntime/">WinPixEventRuntime</a> NuGet package.




## -see-also




<a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a>
 

 

