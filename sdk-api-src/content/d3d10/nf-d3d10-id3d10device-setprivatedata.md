---
UID: NF:d3d10.ID3D10Device.SetPrivateData
title: ID3D10Device::SetPrivateData
author: windows-sdk-content
description: Set data to a device and associate that data with a guid.
old-location: direct3d10\id3d10device_setprivatedata.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_setprivatedata.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: ID3D10Device interface [Direct3D 10],SetPrivateData method, ID3D10Device.SetPrivateData, ID3D10Device::SetPrivateData, SetPrivateData, SetPrivateData method [Direct3D 10], SetPrivateData method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::SetPrivateData, direct3d10.id3d10device_setprivatedata, eaeabbc7-7fa6-0ea4-315b-75d083b44da6
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
 - ID3D10Device.SetPrivateData
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::SetPrivateData


## -description


Set data to a device and associate that data with a guid.


## -parameters




### -param guid [in]

Type: <b><a href="http://msdn.microsoft.com/en-us/library/cc237815(PROT.13).aspx">REFGUID</a></b>

Guid associated with the data.


### -param DataSize [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Size of the data.


### -param pData [in]

Type: <b>const void*</b>

Pointer to the data to be stored with this device. If pData is <b>NULL</b>, DataSize must also be 0, and any data previously associated with the guid will be destroyed.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



The data stored in the device with this method can be retrieved with <a href="https://msdn.microsoft.com/ba0be621-d063-425f-a87f-ded0135c6434">ID3D10DeviceChild::GetPrivateData</a>.

The data and guid set with this method will typically be application-defined.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

