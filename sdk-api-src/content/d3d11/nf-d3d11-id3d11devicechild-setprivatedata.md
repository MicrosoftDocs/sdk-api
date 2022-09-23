---
UID: NF:d3d11.ID3D11DeviceChild.SetPrivateData
title: ID3D11DeviceChild::SetPrivateData (d3d11.h)
description: Set application-defined data to a device child and associate that data with an application-defined guid. (ID3D11DeviceChild.SetPrivateData)
helpviewer_keywords: ["1f73a12c-1aa7-270f-b79f-ea48eb3ec3f5","ID3D11DeviceChild interface [Direct3D 11]","SetPrivateData method","ID3D11DeviceChild.SetPrivateData","ID3D11DeviceChild::SetPrivateData","SetPrivateData","SetPrivateData method [Direct3D 11]","SetPrivateData method [Direct3D 11]","ID3D11DeviceChild interface","d3d11/ID3D11DeviceChild::SetPrivateData","direct3d11.id3d11devicechild_setprivatedata"]
old-location: direct3d11\id3d11devicechild_setprivatedata.htm
tech.root: direct3d11
ms.assetid: 9b5d4c2f-fe1f-4131-9c04-2ea8fae6ee21
ms.date: 12/05/2018
ms.keywords: 1f73a12c-1aa7-270f-b79f-ea48eb3ec3f5, ID3D11DeviceChild interface [Direct3D 11],SetPrivateData method, ID3D11DeviceChild.SetPrivateData, ID3D11DeviceChild::SetPrivateData, SetPrivateData, SetPrivateData method [Direct3D 11], SetPrivateData method [Direct3D 11],ID3D11DeviceChild interface, d3d11/ID3D11DeviceChild::SetPrivateData, direct3d11.id3d11devicechild_setprivatedata
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
 - ID3D11DeviceChild::SetPrivateData
 - d3d11/ID3D11DeviceChild::SetPrivateData
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
 - ID3D11DeviceChild.SetPrivateData
---

# ID3D11DeviceChild::SetPrivateData


## -description

Set application-defined data to a device child and associate that data with an application-defined guid.

## -parameters

### -param guid [in]

Type: <b><a href="/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50">REFGUID</a></b>

Guid associated with the data.

### -param DataSize [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Size of the data.

### -param pData [in, optional]

Type: <b>const void*</b>

Pointer to the data to be stored with this device child. If pData is <b>NULL</b>, DataSize must also be 0, and any data previously associated with the specified guid will be destroyed.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

The data stored in the device child with this method can be retrieved with <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicechild-getprivatedata">ID3D11DeviceChild::GetPrivateData</a>.

The <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers">debug layer</a> reports memory leaks by outputting a list of object interface pointers along with their friendly names. The default friendly name is "&lt;unnamed&gt;". You can set the friendly name so that you can determine if the corresponding object interface pointer caused the leak. To set the friendly name, use the <b>SetPrivateData</b> method and the <b>WKPDID_D3DDebugObjectName</b> GUID that is in D3Dcommon.h. For example, to give pContext a friendly name of <i>My name</i>, use the following code:


```

static const char c_szName[] = "My name";
hr = pContext->SetPrivateData( WKPDID_D3DDebugObjectName, sizeof( c_szName ) - 1, c_szName );

```

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>
