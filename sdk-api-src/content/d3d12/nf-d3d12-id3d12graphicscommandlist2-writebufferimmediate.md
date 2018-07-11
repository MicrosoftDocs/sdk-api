---
UID: NF:d3d12.ID3D12GraphicsCommandList2.WriteBufferImmediate
title: ID3D12GraphicsCommandList2::WriteBufferImmediate
author: windows-sdk-content
description: Writes a number of 32-bit immediate values to the specified buffer locations directly from the command stream.
old-location: direct3d12\id3d12graphicscommandlist2_writebufferimmediate_uint_parameter_mode.htm
old-project: direct3d12
ms.assetid: EB1FD3E0-5785-40D1-961B-AF22F9911653
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: ID3D12GraphicsCommandList2 interface,WriteBufferImmediate method, ID3D12GraphicsCommandList2.WriteBufferImmediate, ID3D12GraphicsCommandList2::WriteBufferImmediate, WriteBufferImmediate, WriteBufferImmediate method, WriteBufferImmediate method,ID3D12GraphicsCommandList2 interface, d3d12/ID3D12GraphicsCommandList2::WriteBufferImmediate, direct3d12.id3d12graphicscommandlist2_writebufferimmediate_uint_parameter_mode
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
 - D3D12.h
api_name:
 - ID3D12GraphicsCommandList2.WriteBufferImmediate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D12GraphicsCommandList2::WriteBufferImmediate


## -description


Writes a number of 32-bit immediate values to the specified buffer locations directly from the command stream.


## -parameters




### -param Count

The number of <a href="https://msdn.microsoft.com/7CF8A888-BB3A-4557-8DA5-7AFAFC6747CF">D3D12_WRITEBUFFERIMMEDIATE_PARAMETER</a> structures that are pointed to by <i>pParams</i> and <i>pModes</i>.


### -param pParams [in]

The address of an array containing a number of <a href="https://msdn.microsoft.com/7CF8A888-BB3A-4557-8DA5-7AFAFC6747CF">D3D12_WRITEBUFFERIMMEDIATE_PARAMETER</a> structures equal to <i>Count</i>.


### -param pModes [in, optional]

The address of an array containing a number of  <a href="https://msdn.microsoft.com/0AB6674C-B73E-4C38-8B6F-18B9BE596B71">D3D12_WRITEBUFFERIMMEDIATE_MODE</a> structures equal to <i>Count</i>. The default value is <b>null</b>; passing <b>null</b> causes the system to write all immediate values using <b>D3D12_WRITEBUFFERIMMEDIATE_MODE_DEFAULT</b>.


## -returns



This method does not return a value.




## -remarks



<b>WriteBufferImmediate</b> performs <i>Count</i> number of 32-bit writes: one for each value and destination specified in <i>pParams</i>.

The receiving buffer (resource) must be in the <b>D3D12_RESOURCE_STATE_COPY_DEST</b> state to be a valid destination for <b>WriteBufferImmediate</b>.




## -see-also




<a href="https://msdn.microsoft.com/6A1BF079-CAE7-45E9-A95F-E19ACD380143">ID3D12GraphicsCommandList2</a>
 

 

