---
UID: NF:d3d12sdklayers.ID3D12DebugDevice1.SetDebugParameter
title: ID3D12DebugDevice1::SetDebugParameter
author: windows-sdk-content
description: Modifies the D3D12 optional device-wide Debug Layer settings.
old-location: direct3d12\id3d12debugdevice1_setdebugparameter.htm
old-project: direct3d12
ms.assetid: D97086C6-CED8-4C4E-ADA1-7A172B3202F3
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: ID3D12DebugDevice1 interface,SetDebugParameter method, ID3D12DebugDevice1.SetDebugParameter, ID3D12DebugDevice1::SetDebugParameter, SetDebugParameter, SetDebugParameter method, SetDebugParameter method,ID3D12DebugDevice1 interface, d3d12sdklayers/ID3D12DebugDevice1::SetDebugParameter, direct3d12.id3d12debugdevice1_setdebugparameter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d12sdklayers.h
req.include-header: 
req.redist: 
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
 - ID3D12DebugDevice1.SetDebugParameter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D12DebugDevice1::SetDebugParameter


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Modifies the D3D12 optional device-wide Debug Layer settings.


## -parameters




### -param Type

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Mt762982(v=VS.85).aspx">D3D12_DEBUG_DEVICE_PARAMETER_TYPE</a></b>

Specifies a <a href="https://msdn.microsoft.com/en-us/library/Mt762982(v=VS.85).aspx">D3D12_DEBUG_DEVICE_PARAMETER_TYPE</a> value that indicates which debug parameter data to get.


### -param pData [in]

Type: <b>const void*</b>

Debug parameter data to set.


### -param DataSize

Type: <b>UINT</b>

Size in bytes of the data pointed to by <i>pData</i>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/en-us/library/Dn706075(v=VS.85).aspx">Direct3D 12 Return Codes</a>. 
          




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt762992(v=VS.85).aspx">GetDebugParameter</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt762990(v=VS.85).aspx">ID3D12DebugDevice1</a>
 

 

