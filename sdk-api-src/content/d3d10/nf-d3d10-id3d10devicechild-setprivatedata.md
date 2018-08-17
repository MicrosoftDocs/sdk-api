---
UID: NF:d3d10.ID3D10DeviceChild.SetPrivateData
title: ID3D10DeviceChild::SetPrivateData
author: windows-sdk-content
description: Set application-defined data to a device child and associate that data with an application-defined guid.
old-location: direct3d10\id3d10devicechild_setprivatedata.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10devicechild_setprivatedata.htm
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: ID3D10DeviceChild interface [Direct3D 10],SetPrivateData method, ID3D10DeviceChild.SetPrivateData, ID3D10DeviceChild::SetPrivateData, SetPrivateData, SetPrivateData method [Direct3D 10], SetPrivateData method [Direct3D 10],ID3D10DeviceChild interface, b8fdde8d-dc47-4ec2-997e-b42841dc5441, d3d10/ID3D10DeviceChild::SetPrivateData, direct3d10.id3d10devicechild_setprivatedata
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10.h
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
req.typenames: D3D10_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10DeviceChild.SetPrivateData
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10DeviceChild::SetPrivateData


## -description


Set application-defined data to a device child and associate that data with an application-defined guid.


## -parameters




### -param guid [in]

Type: <b><a href="http://msdn.microsoft.com/en-us/library/cc237815(PROT.13).aspx">REFGUID</a></b>

Guid associated with the data.


### -param DataSize [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Size of the data.


### -param pData [in]

Type: <b>const void*</b>

Pointer to the data to be stored with this device child. If pData is <b>NULL</b>, DataSize must also be 0, and any data previously associated with the specified guid will be destroyed.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



The data stored in the device child with this method can be retrieved with <a href="https://msdn.microsoft.com/en-us/library/Bb173531(v=VS.85).aspx">ID3D10DeviceChild::GetPrivateData</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173529(v=VS.85).aspx">ID3D10DeviceChild Interface</a>
 

 

