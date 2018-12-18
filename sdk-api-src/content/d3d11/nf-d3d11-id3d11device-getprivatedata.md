---
UID: NF:d3d11.ID3D11Device.GetPrivateData
title: ID3D11Device::GetPrivateData
author: windows-sdk-content
description: Get application-defined data from a device.
old-location: direct3d11\id3d11device_getprivatedata.htm
tech.root: direct3d11
ms.assetid: 8aeb004e-4507-4bf4-bd79-2747feaf5e4d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetPrivateData, GetPrivateData method [Direct3D 11], GetPrivateData method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],GetPrivateData method, ID3D11Device.GetPrivateData, ID3D11Device::GetPrivateData, cd04b276-e229-c087-80d8-decc870a424f, d3d11/ID3D11Device::GetPrivateData, direct3d11.id3d11device_getprivatedata
ms.topic: method
req.header: d3d11.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Device.GetPrivateData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11Device::GetPrivateData


## -description


Get application-defined data from a device.


## -parameters




### -param guid [in]

Type: <b><a href="http://msdn.microsoft.com/en-us/library/cc237815(PROT.13).aspx">REFGUID</a></b>

Guid associated with the data.


### -param pDataSize [in, out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

A pointer to a variable that on input contains the size, in bytes, of the buffer that <i>pData</i> points to, and on output contains the size, in bytes, of the amount of data that <b>GetPrivateData</b> retrieved.


### -param pData [out, optional]

Type: <b>void*</b>

A pointer to a buffer that <b>GetPrivateData</b>  fills with data from the device if <i>pDataSize</i> points to a value that specifies a buffer large enough to hold the data.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the codes described in the topic <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>
 

 

