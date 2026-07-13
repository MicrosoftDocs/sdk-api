---
UID: NF:d3d10.ID3D10DeviceChild.GetPrivateData
title: ID3D10DeviceChild::GetPrivateData (d3d10.h)
description: Get application-defined data from a device child. (ID3D10DeviceChild.GetPrivateData)
helpviewer_keywords: ["1156e7b1-1ba9-fab9-ab1a-7695c94278e9","GetPrivateData","GetPrivateData method [Direct3D 10]","GetPrivateData method [Direct3D 10]","ID3D10DeviceChild interface","ID3D10DeviceChild interface [Direct3D 10]","GetPrivateData method","ID3D10DeviceChild.GetPrivateData","ID3D10DeviceChild::GetPrivateData","d3d10/ID3D10DeviceChild::GetPrivateData","direct3d10.id3d10devicechild_getprivatedata"]
old-location: direct3d10\id3d10devicechild_getprivatedata.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10devicechild_getprivatedata.htm
ms.date: 12/05/2018
ms.keywords: 1156e7b1-1ba9-fab9-ab1a-7695c94278e9, GetPrivateData, GetPrivateData method [Direct3D 10], GetPrivateData method [Direct3D 10],ID3D10DeviceChild interface, ID3D10DeviceChild interface [Direct3D 10],GetPrivateData method, ID3D10DeviceChild.GetPrivateData, ID3D10DeviceChild::GetPrivateData, d3d10/ID3D10DeviceChild::GetPrivateData, direct3d10.id3d10devicechild_getprivatedata
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
 - ID3D10DeviceChild::GetPrivateData
 - d3d10/ID3D10DeviceChild::GetPrivateData
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
 - ID3D10DeviceChild.GetPrivateData
---

# ID3D10DeviceChild::GetPrivateData


## -description

Get application-defined data from a device child.

## -parameters

### -param guid [in]

Type: <b><a href="/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50">REFGUID</a></b>

Guid associated with the data.

### -param pDataSize [in, out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

Size of the data.

### -param pData [out]

Type: <b>void*</b>

Pointer to the data stored with the device child. If pData is <b>NULL</b>, DataSize must also be 0, and any data previously associated with the guid will be destroyed.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

If the data returned is a pointer to an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>, or one of its derivative classes, which was previously set by **SetPrivateDataInterface**, that interface will have its reference count incremented before the private data is returned.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10devicechild">ID3D10DeviceChild Interface</a>
