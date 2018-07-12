---
UID: NS:d3d12.D3D12_STREAM_OUTPUT_DESC
title: D3D12_STREAM_OUTPUT_DESC
author: windows-sdk-content
description: Describes a streaming output buffer.
old-location: direct3d12\d3d12_stream_output_desc.htm
old-project: direct3d12
ms.assetid: 9EFAA901-857B-40E3-B4B7-7C04D53BCA67
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: D3D12_STREAM_OUTPUT_DESC, D3D12_STREAM_OUTPUT_DESC structure, d3d12/D3D12_STREAM_OUTPUT_DESC, direct3d12.d3d12_stream_output_desc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: D3D12_STREAM_OUTPUT_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_STREAM_OUTPUT_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_STREAM_OUTPUT_DESC structure


## -description


Describes a streaming output buffer.


## -struct-fields




### -field pSODeclaration


            An array of <a href="https://msdn.microsoft.com/F16FA746-2213-4F11-85AD-2CDCB0744618">D3D12_SO_DECLARATION_ENTRY</a> structures. Can't be <b>NULL</b> if <b>NumEntries</b> &gt; 0.
          


### -field NumEntries


            The number of entries in the stream output declaration array that the <b>pSODeclaration</b> member points to.
          


### -field pBufferStrides


            An array of buffer strides; each stride is the size of an element for that buffer.
          


### -field NumStrides


            The number of strides (or buffers) that the <b>pBufferStrides</b> member points to.
          


### -field RasterizedStream


            The index number of the stream to be sent to the rasterizer stage.
          


## -remarks




        A <a href="https://msdn.microsoft.com/35D10150-A633-4D38-B684-3E2DF357FFC0">D3D12_GRAPHICS_PIPELINE_STATE_DESC</a> object contains a <b>D3D12_STREAM_OUTPUT_DESC</b> structure.
      




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

