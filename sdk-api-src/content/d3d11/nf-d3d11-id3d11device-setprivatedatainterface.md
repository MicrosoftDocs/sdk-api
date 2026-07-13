---
UID: NF:d3d11.ID3D11Device.SetPrivateDataInterface
title: ID3D11Device::SetPrivateDataInterface (d3d11.h)
description: Associate an IUnknown-derived interface with this device child and associate that interface with an application-defined guid. (ID3D11Device.SetPrivateDataInterface)
helpviewer_keywords: ["ID3D11Device interface [Direct3D 11]","SetPrivateDataInterface method","ID3D11Device.SetPrivateDataInterface","ID3D11Device::SetPrivateDataInterface","SetPrivateDataInterface","SetPrivateDataInterface method [Direct3D 11]","SetPrivateDataInterface method [Direct3D 11]","ID3D11Device interface","c27aaa23-b80d-2dcf-0f00-1b62c5fb3acb","d3d11/ID3D11Device::SetPrivateDataInterface","direct3d11.id3d11device_setprivatedatainterface"]
old-location: direct3d11\id3d11device_setprivatedatainterface.htm
tech.root: direct3d11
ms.assetid: 65b4461d-bfbb-4de1-84f8-6294fde12980
ms.date: 12/05/2018
ms.keywords: ID3D11Device interface [Direct3D 11],SetPrivateDataInterface method, ID3D11Device.SetPrivateDataInterface, ID3D11Device::SetPrivateDataInterface, SetPrivateDataInterface, SetPrivateDataInterface method [Direct3D 11], SetPrivateDataInterface method [Direct3D 11],ID3D11Device interface, c27aaa23-b80d-2dcf-0f00-1b62c5fb3acb, d3d11/ID3D11Device::SetPrivateDataInterface, direct3d11.id3d11device_setprivatedatainterface
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
 - ID3D11Device::SetPrivateDataInterface
 - d3d11/ID3D11Device::SetPrivateDataInterface
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
 - ID3D11Device.SetPrivateDataInterface
---

# ID3D11Device::SetPrivateDataInterface


## -description

Associate an IUnknown-derived interface with this device child and associate that interface with an application-defined guid.

## -parameters

### -param guid [in]

Type: <b><a href="/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50">REFGUID</a></b>

Guid associated with the interface.

### -param pData [in, optional]

Type: <b>const IUnknown*</b>

A pointer to the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)-derived interface to be associated with the device object. Its reference count is incremented when set, and decremented when either the [ID3D11Device](/windows/win32/api/d3d11/nn-d3d11-id3d11device) is destroyed, or when the data is overwritten by calling [SetPrivateData](/windows/win32/api/d3d11/nf-d3d11-id3d11device-setprivatedata) or **SetPrivateDataInterface** with the same **GUID**.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>
