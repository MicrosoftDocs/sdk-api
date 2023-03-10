---
UID: NF:d3d10.ID3D10Device.SetPrivateData
title: ID3D10Device::SetPrivateData (d3d10.h)
description: Set data to a device and associate that data with a guid. (ID3D10Device.SetPrivateData)
helpviewer_keywords: ["ID3D10Device interface [Direct3D 10]","SetPrivateData method","ID3D10Device.SetPrivateData","ID3D10Device::SetPrivateData","SetPrivateData","SetPrivateData method [Direct3D 10]","SetPrivateData method [Direct3D 10]","ID3D10Device interface","d3d10/ID3D10Device::SetPrivateData","direct3d10.id3d10device_setprivatedata","eaeabbc7-7fa6-0ea4-315b-75d083b44da6"]
old-location: direct3d10\id3d10device_setprivatedata.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_setprivatedata.htm
ms.date: 12/05/2018
ms.keywords: ID3D10Device interface [Direct3D 10],SetPrivateData method, ID3D10Device.SetPrivateData, ID3D10Device::SetPrivateData, SetPrivateData, SetPrivateData method [Direct3D 10], SetPrivateData method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::SetPrivateData, direct3d10.id3d10device_setprivatedata, eaeabbc7-7fa6-0ea4-315b-75d083b44da6
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Device::SetPrivateData
 - d3d10/ID3D10Device::SetPrivateData
dev_langs:
 - c++
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
---

# ID3D10Device::SetPrivateData


## -description

Set data to a device and associate that data with a guid.

## -parameters

### -param guid [in]

Type: <b><a href="/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50">REFGUID</a></b>

Guid associated with the data.

### -param DataSize [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Size of the data.

### -param pData [in]

Type: <b>const void*</b>

Pointer to the data to be stored with this device. If pData is <b>NULL</b>, DataSize must also be 0, and any data previously associated with the guid will be destroyed.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

The data stored in the device with this method can be retrieved with <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-getprivatedata">ID3D10DeviceChild::GetPrivateData</a>.

The data and guid set with this method will typically be application-defined.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
