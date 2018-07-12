---
UID: NF:d3d10.ID3D10Device.GetPrivateData
title: ID3D10Device::GetPrivateData
author: windows-sdk-content
description: Get data from a device that is associated with a guid.
old-location: direct3d10\id3d10device_getprivatedata.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_getprivatedata.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: 21f7168b-1fad-e566-5ab6-9dcae79a06ca, GetPrivateData, GetPrivateData method [Direct3D 10], GetPrivateData method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],GetPrivateData method, ID3D10Device.GetPrivateData, ID3D10Device::GetPrivateData, d3d10/ID3D10Device::GetPrivateData, direct3d10.id3d10device_getprivatedata
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10.h
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
 - ID3D10Device.GetPrivateData
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::GetPrivateData


## -description


Get data from a device that is associated with a guid.


## -parameters




### -param guid [in]

Type: <b><a href="http://msdn.microsoft.com/en-us/library/cc237815(PROT.13).aspx">REFGUID</a></b>

Guid associated with the data.


### -param pDataSize [in, out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

Size of the data.


### -param pData [out]

Type: <b>void*</b>

Pointer to the data stored with the device. If pData is <b>NULL</b>, DataSize must also be 0, and any data previously associated with the guid will be destroyed.


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



The data stored in the device is set with <a href="https://msdn.microsoft.com/library/Bb173616(v=VS.85).aspx">ID3D10Device::SetPrivateData</a>. 

The data retrieved and the guid will typically be application-defined.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

