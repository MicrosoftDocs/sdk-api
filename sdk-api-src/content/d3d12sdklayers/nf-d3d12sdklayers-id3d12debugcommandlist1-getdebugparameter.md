---
UID: NF:d3d12sdklayers.ID3D12DebugCommandList1.GetDebugParameter
title: ID3D12DebugCommandList1::GetDebugParameter
author: windows-sdk-content
description: Gets optional Command List Debug Layer settings.
old-location: direct3d12\id3d12debugcommandlist1_getdebugparameter.htm
old-project: direct3d12
ms.assetid: 936E9748-1D1A-46A9-B4FE-36C0C6627296
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetDebugParameter, GetDebugParameter method, GetDebugParameter method,ID3D12DebugCommandList1 interface, ID3D12DebugCommandList1 interface,GetDebugParameter method, ID3D12DebugCommandList1.GetDebugParameter, ID3D12DebugCommandList1::GetDebugParameter, d3d12sdklayers/ID3D12DebugCommandList1::GetDebugParameter, direct3d12.id3d12debugcommandlist1_getdebugparameter
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D12_RLDO_FLAGS
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
req.lib: 
req.dll: 
req.irql: 
---

# ID3D12DebugCommandList1::GetDebugParameter


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Gets optional Command List Debug Layer settings.


## -parameters




### -param Type

Type: <b><a href="https://msdn.microsoft.com/ED8E6A7C-4D30-4396-B2D6-C09C18284B4D">D3D12_DEBUG_COMMAND_LIST_PARAMETER_TYPE</a></b>

Specifies a <a href="https://msdn.microsoft.com/ED8E6A7C-4D30-4396-B2D6-C09C18284B4D">D3D12_DEBUG_COMMAND_LIST_PARAMETER_TYPE</a> value that determines which debug parameter data to copy to the memory pointed to by <i>pData</i>.


### -param pData [out]

Type: <b>void*</b>

Points to the memory that will be filled with a copy of the debug parameter data. The interpretation of this data depends on the <a href="https://msdn.microsoft.com/ED8E6A7C-4D30-4396-B2D6-C09C18284B4D">D3D12_DEBUG_COMMAND_LIST_PARAMETER_TYPE</a> given in the <i>Type</i> parameter.


### -param DataSize

Type: <b>UINT</b>

Size in bytes of the memory buffer pointed to by <i>pData</i>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>


            Returns S_OK if successful, otherwise E_INVALIDARG. 
          




## -see-also




<a href="https://msdn.microsoft.com/2DF22383-768C-4D23-9ED8-F0CFD6BA6EE7">ID3D12DebugCommandList1</a>



<a href="https://msdn.microsoft.com/8D93895A-BED7-4A86-893B-ACB5FA1B160F">SetDebugParameter</a>
 

 

