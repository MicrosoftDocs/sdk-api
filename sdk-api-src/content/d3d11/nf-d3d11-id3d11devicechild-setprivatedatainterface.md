---
UID: NF:d3d11.ID3D11DeviceChild.SetPrivateDataInterface
title: ID3D11DeviceChild::SetPrivateDataInterface
author: windows-sdk-content
description: Associate an IUnknown-derived interface with this device child and associate that interface with an application-defined guid.
old-location: direct3d11\id3d11devicechild_setprivatedatainterface.htm
tech.root: direct3d11
ms.assetid: 18b7daa3-a727-474d-836e-f47a56d39c89
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 7c5c6bc1-57d6-90b3-4715-5f6dbe8653c2, ID3D11DeviceChild interface [Direct3D 11],SetPrivateDataInterface method, ID3D11DeviceChild.SetPrivateDataInterface, ID3D11DeviceChild::SetPrivateDataInterface, SetPrivateDataInterface, SetPrivateDataInterface method [Direct3D 11], SetPrivateDataInterface method [Direct3D 11],ID3D11DeviceChild interface, d3d11/ID3D11DeviceChild::SetPrivateDataInterface, direct3d11.id3d11devicechild_setprivatedatainterface
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
 - ID3D11DeviceChild.SetPrivateDataInterface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d11.h
: 
- ID3D11DeviceChild.SetPrivateDataInterface
: 
---

# ID3D11DeviceChild::SetPrivateDataInterface


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



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -remarks



When this method is called ::addref() will be called on the IUnknown-derived interface, and when the device child is detroyed ::release() will be called on the IUnknown-derived interface.




## -see-also




<a href="https://msdn.microsoft.com/bed17239-0358-4768-8655-9a1d92f25a2e">ID3D11DeviceChild</a>
 

 

