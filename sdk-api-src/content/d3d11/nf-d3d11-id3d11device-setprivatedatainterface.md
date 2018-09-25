---
UID: NF:d3d11.ID3D11Device.SetPrivateDataInterface
title: ID3D11Device::SetPrivateDataInterface
author: windows-sdk-content
description: Associate an IUnknown-derived interface with this device child and associate that interface with an application-defined guid.
old-location: direct3d11\id3d11device_setprivatedatainterface.htm
tech.root: direct3d11
ms.assetid: 65b4461d-bfbb-4de1-84f8-6294fde12980
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ID3D11Device interface [Direct3D 11],SetPrivateDataInterface method, ID3D11Device.SetPrivateDataInterface, ID3D11Device::SetPrivateDataInterface, SetPrivateDataInterface, SetPrivateDataInterface method [Direct3D 11], SetPrivateDataInterface method [Direct3D 11],ID3D11Device interface, c27aaa23-b80d-2dcf-0f00-1b62c5fb3acb, d3d11/ID3D11Device::SetPrivateDataInterface, direct3d11.id3d11device_setprivatedatainterface
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ID3D11Device.SetPrivateDataInterface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11Device::SetPrivateDataInterface


## -description


Associate an IUnknown-derived interface with this device child and associate that interface with an application-defined guid.


## -parameters




### -param guid [in]

Type: <b><a href="http://msdn.microsoft.com/en-us/library/cc237815(PROT.13).aspx">REFGUID</a></b>

Guid associated with the interface.


### -param pData [in, optional]

Type: <b>const IUnknown*</b>

Pointer to an IUnknown-derived interface to be associated with the device child.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>
 

 

