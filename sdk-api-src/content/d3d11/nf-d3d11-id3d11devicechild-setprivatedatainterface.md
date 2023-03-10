---
UID: NF:d3d11.ID3D11DeviceChild.SetPrivateDataInterface
title: ID3D11DeviceChild::SetPrivateDataInterface (d3d11.h)
description: Associate an IUnknown-derived interface with this device child and associate that interface with an application-defined guid. (ID3D11DeviceChild.SetPrivateDataInterface)
helpviewer_keywords: ["7c5c6bc1-57d6-90b3-4715-5f6dbe8653c2","ID3D11DeviceChild interface [Direct3D 11]","SetPrivateDataInterface method","ID3D11DeviceChild.SetPrivateDataInterface","ID3D11DeviceChild::SetPrivateDataInterface","SetPrivateDataInterface","SetPrivateDataInterface method [Direct3D 11]","SetPrivateDataInterface method [Direct3D 11]","ID3D11DeviceChild interface","d3d11/ID3D11DeviceChild::SetPrivateDataInterface","direct3d11.id3d11devicechild_setprivatedatainterface"]
old-location: direct3d11\id3d11devicechild_setprivatedatainterface.htm
tech.root: direct3d11
ms.assetid: 18b7daa3-a727-474d-836e-f47a56d39c89
ms.date: 12/05/2018
ms.keywords: 7c5c6bc1-57d6-90b3-4715-5f6dbe8653c2, ID3D11DeviceChild interface [Direct3D 11],SetPrivateDataInterface method, ID3D11DeviceChild.SetPrivateDataInterface, ID3D11DeviceChild::SetPrivateDataInterface, SetPrivateDataInterface, SetPrivateDataInterface method [Direct3D 11], SetPrivateDataInterface method [Direct3D 11],ID3D11DeviceChild interface, d3d11/ID3D11DeviceChild::SetPrivateDataInterface, direct3d11.id3d11devicechild_setprivatedatainterface
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11DeviceChild::SetPrivateDataInterface
 - d3d11/ID3D11DeviceChild::SetPrivateDataInterface
dev_langs:
 - c++
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
---

# ID3D11DeviceChild::SetPrivateDataInterface


## -description

Associate an IUnknown-derived interface with this device child and associate that interface with an application-defined guid.

## -parameters

### -param guid [in]

Type: <b><a href="/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50">REFGUID</a></b>

Guid associated with the interface.

### -param pData [in, optional]

Type: <b>const IUnknown*</b>

Pointer to an IUnknown-derived interface to be associated with the device child.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

When this method is called ::addref() will be called on the IUnknown-derived interface, and when the device child is destroyed ::release() will be called on the IUnknown-derived interface.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>
