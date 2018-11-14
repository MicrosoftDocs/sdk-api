---
UID: NF:d3d12sdklayers.ID3D12DebugCommandList1.GetDebugParameter
title: ID3D12DebugCommandList1::GetDebugParameter
author: windows-sdk-content
description: Gets optional Command List Debug Layer settings.
old-location: direct3d12\id3d12debugcommandlist1_getdebugparameter.htm
tech.root: direct3d12
ms.assetid: 936E9748-1D1A-46A9-B4FE-36C0C6627296
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: GetDebugParameter, GetDebugParameter method, GetDebugParameter method,ID3D12DebugCommandList1 interface, ID3D12DebugCommandList1 interface,GetDebugParameter method, ID3D12DebugCommandList1.GetDebugParameter, ID3D12DebugCommandList1::GetDebugParameter, d3d12sdklayers/ID3D12DebugCommandList1::GetDebugParameter, direct3d12.id3d12debugcommandlist1_getdebugparameter
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
 - ID3D12DebugCommandList1.GetDebugParameter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d12sdklayers.h
: 
- ID3D12DebugCommandList1.GetDebugParameter
: 
---

# ID3D12DebugCommandList1::GetDebugParameter


## -description


Gets optional Command List Debug Layer settings.


## -parameters




### -param Type

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Mt762980(v=VS.85).aspx">D3D12_DEBUG_COMMAND_LIST_PARAMETER_TYPE</a></b>

Specifies a <a href="https://msdn.microsoft.com/en-us/library/Mt762980(v=VS.85).aspx">D3D12_DEBUG_COMMAND_LIST_PARAMETER_TYPE</a> value that determines which debug parameter data to copy to the memory pointed to by <i>pData</i>.


### -param pData [out]

Type: <b>void*</b>

Points to the memory that will be filled with a copy of the debug parameter data. The interpretation of this data depends on the <a href="https://msdn.microsoft.com/en-us/library/Mt762980(v=VS.85).aspx">D3D12_DEBUG_COMMAND_LIST_PARAMETER_TYPE</a> given in the <i>Type</i> parameter.


### -param DataSize

Type: <b>UINT</b>

Size in bytes of the memory buffer pointed to by <i>pData</i>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns S_OK if successful, otherwise E_INVALIDARG. 
          




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt762986(v=VS.85).aspx">ID3D12DebugCommandList1</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt762989(v=VS.85).aspx">SetDebugParameter</a>
 

 

