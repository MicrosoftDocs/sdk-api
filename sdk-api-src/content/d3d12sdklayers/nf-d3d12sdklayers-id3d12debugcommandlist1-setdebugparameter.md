---
UID: NF:d3d12sdklayers.ID3D12DebugCommandList1.SetDebugParameter
title: ID3D12DebugCommandList1::SetDebugParameter
author: windows-sdk-content
description: Modifies optional Debug Layer settings of a command list.
old-location: direct3d12\id3d12debugcommandlist1_setdebugparameter.htm
tech.root: direct3d12
ms.assetid: 8D93895A-BED7-4A86-893B-ACB5FA1B160F
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: ID3D12DebugCommandList1 interface,SetDebugParameter method, ID3D12DebugCommandList1.SetDebugParameter, ID3D12DebugCommandList1::SetDebugParameter, SetDebugParameter, SetDebugParameter method, SetDebugParameter method,ID3D12DebugCommandList1 interface, d3d12sdklayers/ID3D12DebugCommandList1::SetDebugParameter, direct3d12.id3d12debugcommandlist1_setdebugparameter
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
 - ID3D12DebugCommandList1.SetDebugParameter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12DebugCommandList1::SetDebugParameter


## -description


Modifies optional Debug Layer settings of a command list.


## -parameters




### -param Type

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Mt762980(v=VS.85).aspx">D3D12_DEBUG_COMMAND_LIST_PARAMETER_TYPE</a></b>

Specifies a <a href="https://msdn.microsoft.com/en-us/library/Mt762980(v=VS.85).aspx">D3D12_DEBUG_COMMAND_LIST_PARAMETER_TYPE</a> value that indicates which debug parameter data to set.


### -param pData [in]

Type: <b>const void*</b>

Pointer to debug parameter data to set.  The interpretation of this data depends on the <a href="https://msdn.microsoft.com/en-us/library/Mt762980(v=VS.85).aspx">D3D12_DEBUG_COMMAND_LIST_PARAMETER_TYPE</a> given in the <i>Type</i> parameter.


### -param DataSize

Type: <b>UINT</b>

Specifies the size in bytes of the debug parameter <i>pData</i>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/en-us/library/Dn706075(v=VS.85).aspx">Direct3D 12 Return Codes</a>. 
          




## -remarks



Certain debug behaviors of D3D12 Debug Layer can be modified by setting debug parameters.  These can be used to toggle extra validation or expose experimental debug features.

<b>ID3D12DebugCommandList1::SetDebugParameter</b> only impacts debug settings for the associated command list.  For device-wide debug parameters see the <a href="https://msdn.microsoft.com/en-us/library/Mt762994(v=VS.85).aspx">ID3D12DebugDevice1::SetDebugParameter</a> method.

Resetting a command list restores the debug parameters to the default values.  This is because a command list reset is treated as equivalent to creating a new command list.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt762988(v=VS.85).aspx">GetDebugParameter</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt762986(v=VS.85).aspx">ID3D12DebugCommandList1</a>
 

 

