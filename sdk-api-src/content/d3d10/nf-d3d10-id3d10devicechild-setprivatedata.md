---
UID: NF:d3d10.ID3D10DeviceChild.SetPrivateData
title: ID3D10DeviceChild::SetPrivateData (d3d10.h)
description: Set application-defined data to a device child and associate that data with an application-defined guid. (ID3D10DeviceChild.SetPrivateData)
helpviewer_keywords: ["ID3D10DeviceChild interface [Direct3D 10]","SetPrivateData method","ID3D10DeviceChild.SetPrivateData","ID3D10DeviceChild::SetPrivateData","SetPrivateData","SetPrivateData method [Direct3D 10]","SetPrivateData method [Direct3D 10]","ID3D10DeviceChild interface","b8fdde8d-dc47-4ec2-997e-b42841dc5441","d3d10/ID3D10DeviceChild::SetPrivateData","direct3d10.id3d10devicechild_setprivatedata"]
old-location: direct3d10\id3d10devicechild_setprivatedata.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10devicechild_setprivatedata.htm
ms.date: 12/05/2018
ms.keywords: ID3D10DeviceChild interface [Direct3D 10],SetPrivateData method, ID3D10DeviceChild.SetPrivateData, ID3D10DeviceChild::SetPrivateData, SetPrivateData, SetPrivateData method [Direct3D 10], SetPrivateData method [Direct3D 10],ID3D10DeviceChild interface, b8fdde8d-dc47-4ec2-997e-b42841dc5441, d3d10/ID3D10DeviceChild::SetPrivateData, direct3d10.id3d10devicechild_setprivatedata
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
 - ID3D10DeviceChild::SetPrivateData
 - d3d10/ID3D10DeviceChild::SetPrivateData
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
 - ID3D10DeviceChild.SetPrivateData
---

# ID3D10DeviceChild::SetPrivateData


## -description

Set application-defined data to a device child and associate that data with an application-defined guid.

## -parameters

### -param guid [in]

Type: <b><a href="/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50">REFGUID</a></b>

Guid associated with the data.

### -param DataSize [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Size of the data.

### -param pData [in]

Type: <b>const void*</b>

Pointer to the data to be stored with this device child. If pData is <b>NULL</b>, DataSize must also be 0, and any data previously associated with the specified guid will be destroyed.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

The data stored in the device child with this method can be retrieved with <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10devicechild-getprivatedata">ID3D10DeviceChild::GetPrivateData</a>.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10devicechild">ID3D10DeviceChild Interface</a>
