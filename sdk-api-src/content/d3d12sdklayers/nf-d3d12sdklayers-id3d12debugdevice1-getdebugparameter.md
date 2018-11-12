---
UID: NF:d3d12sdklayers.ID3D12DebugDevice1.GetDebugParameter
title: ID3D12DebugDevice1::GetDebugParameter
author: windows-sdk-content
description: Gets optional device-wide Debug Layer settings.
old-location: direct3d12\id3d12debugdevice1_getdebugparameter.htm
tech.root: direct3d12
ms.assetid: 13A7E7D6-FF00-4E17-A7C5-C383F93F6A06
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetDebugParameter, GetDebugParameter method, GetDebugParameter method,ID3D12DebugDevice1 interface, ID3D12DebugDevice1 interface,GetDebugParameter method, ID3D12DebugDevice1.GetDebugParameter, ID3D12DebugDevice1::GetDebugParameter, d3d12sdklayers/ID3D12DebugDevice1::GetDebugParameter, direct3d12.id3d12debugdevice1_getdebugparameter
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
 - ID3D12DebugDevice1.GetDebugParameter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12DebugDevice1::GetDebugParameter


## -description


Gets optional device-wide Debug Layer settings.


## -parameters




### -param Type

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Mt762982(v=VS.85).aspx">D3D12_DEBUG_DEVICE_PARAMETER_TYPE</a></b>

Specifies a <a href="https://msdn.microsoft.com/en-us/library/Mt762982(v=VS.85).aspx">D3D12_DEBUG_DEVICE_PARAMETER_TYPE</a> value that indicates which debug parameter data to set.


### -param pData [out]

Type: <b>void*</b>

Points to the memory that will be filled with a copy of the debug parameter data. The interpretation of this data depends on the <a href="https://msdn.microsoft.com/en-us/library/Mt762982(v=VS.85).aspx">D3D12_DEBUG_DEVICE_PARAMETER_TYPE</a> given in the <i>Type</i> parameter.


### -param DataSize

Type: <b>UINT</b>

Size in bytes of the memory buffer pointed to by <i>pData</i>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/en-us/library/Dn706075(v=VS.85).aspx">Direct3D 12 Return Codes</a>. 
          




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt762990(v=VS.85).aspx">ID3D12DebugDevice1</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt762994(v=VS.85).aspx">SetDebugParameter</a>
 

 

