---
UID: NF:d3d11.ID3D11Device.GetPrivateData
title: ID3D11Device::GetPrivateData (d3d11.h)
description: Get application-defined data from a device.
helpviewer_keywords: ["GetPrivateData","GetPrivateData method [Direct3D 11]","GetPrivateData method [Direct3D 11]","ID3D11Device interface","ID3D11Device interface [Direct3D 11]","GetPrivateData method","ID3D11Device.GetPrivateData","ID3D11Device::GetPrivateData","cd04b276-e229-c087-80d8-decc870a424f","d3d11/ID3D11Device::GetPrivateData","direct3d11.id3d11device_getprivatedata"]
old-location: direct3d11\id3d11device_getprivatedata.htm
tech.root: direct3d11
ms.assetid: 8aeb004e-4507-4bf4-bd79-2747feaf5e4d
ms.date: 12/05/2018
ms.keywords: GetPrivateData, GetPrivateData method [Direct3D 11], GetPrivateData method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],GetPrivateData method, ID3D11Device.GetPrivateData, ID3D11Device::GetPrivateData, cd04b276-e229-c087-80d8-decc870a424f, d3d11/ID3D11Device::GetPrivateData, direct3d11.id3d11device_getprivatedata
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
 - ID3D11Device::GetPrivateData
 - d3d11/ID3D11Device::GetPrivateData
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
 - ID3D11Device.GetPrivateData
---

# ID3D11Device::GetPrivateData


## -description

Get application-defined data from a device.

## -parameters

### -param guid [in]

Type: <b><a href="/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50">REFGUID</a></b>

Guid associated with the data.

### -param pDataSize [in, out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

A pointer to a variable that on input contains the size, in bytes, of the buffer that <i>pData</i> points to, and on output contains the size, in bytes, of the amount of data that <b>GetPrivateData</b> retrieved.

### -param pData [out, optional]

Type: <b>void*</b>

A pointer to a buffer that <b>GetPrivateData</b>  fills with data from the device if <i>pDataSize</i> points to a value that specifies a buffer large enough to hold the data.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the codes described in the topic <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

If the data returned is a pointer to an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>, or one of its derivative classes, which was previously set by **SetPrivateDataInterface**, that interface will have its reference count incremented before the private data is returned.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>