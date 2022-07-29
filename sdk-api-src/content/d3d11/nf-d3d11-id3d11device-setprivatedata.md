---
UID: NF:d3d11.ID3D11Device.SetPrivateData
title: ID3D11Device::SetPrivateData (d3d11.h)
description: Set data to a device and associate that data with a guid. (ID3D11Device.SetPrivateData)
helpviewer_keywords: ["ID3D11Device interface [Direct3D 11]","SetPrivateData method","ID3D11Device.SetPrivateData","ID3D11Device::SetPrivateData","SetPrivateData","SetPrivateData method [Direct3D 11]","SetPrivateData method [Direct3D 11]","ID3D11Device interface","d3d11/ID3D11Device::SetPrivateData","direct3d11.id3d11device_setprivatedata","f1172c7e-62ba-f206-04b7-7dc3e29d9d16"]
old-location: direct3d11\id3d11device_setprivatedata.htm
tech.root: direct3d11
ms.assetid: 0a8add57-b209-4096-9132-f3258469bdbd
ms.date: 12/05/2018
ms.keywords: ID3D11Device interface [Direct3D 11],SetPrivateData method, ID3D11Device.SetPrivateData, ID3D11Device::SetPrivateData, SetPrivateData, SetPrivateData method [Direct3D 11], SetPrivateData method [Direct3D 11],ID3D11Device interface, d3d11/ID3D11Device::SetPrivateData, direct3d11.id3d11device_setprivatedata, f1172c7e-62ba-f206-04b7-7dc3e29d9d16
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
 - ID3D11Device::SetPrivateData
 - d3d11/ID3D11Device::SetPrivateData
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
 - ID3D11Device.SetPrivateData
---

# ID3D11Device::SetPrivateData


## -description

Set data to a device and associate that data with a guid.

## -parameters

### -param guid [in]

Type: <b><a href="/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50">REFGUID</a></b>

Guid associated with the data.

### -param DataSize [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Size of the data.

### -param pData [in, optional]

Type: <b>const void*</b>

Pointer to the data to be stored with this device. If pData is <b>NULL</b>, DataSize must also be 0, and any data previously associated with the guid will be destroyed.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

The data stored in the device with this method can be retrieved with <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-getprivatedata">ID3D11Device::GetPrivateData</a>.

The data and guid set with this method will typically be application-defined.

The <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers">debug layer</a> reports memory leaks by outputting a list of object interface pointers along with their friendly names. The default friendly name is "&lt;unnamed&gt;". You can set the friendly name so that you can determine if the corresponding object interface pointer caused the leak. To set the friendly name, use the <b>SetPrivateData</b> method and the <b>WKPDID_D3DDebugObjectName</b> GUID that is in D3Dcommon.h. For example, to give pContext a friendly name of <i>My name</i>, use the following code:


```

static const char c_szName[] = "My name";
hr = pContext->SetPrivateData( WKPDID_D3DDebugObjectName, sizeof( c_szName ) - 1, c_szName );

```

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>
