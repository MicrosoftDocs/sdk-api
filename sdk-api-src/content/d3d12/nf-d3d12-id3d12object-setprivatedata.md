---
UID: NF:d3d12.ID3D12Object.SetPrivateData
title: ID3D12Object::SetPrivateData (d3d12.h)
description: Sets application-defined data to a device object and associates that data with an application-defined GUID.
helpviewer_keywords: ["ID3D12Object interface","SetPrivateData method","ID3D12Object.SetPrivateData","ID3D12Object::SetPrivateData","SetPrivateData","SetPrivateData method","SetPrivateData method","ID3D12Object interface","d3d12/ID3D12Object::SetPrivateData","direct3d12.id3d12object_setprivatedata"]
old-location: direct3d12\id3d12object_setprivatedata.htm
tech.root: direct3d12
ms.assetid: 1B3E8202-7CB3-4D9F-A1AE-70E66652773C
ms.date: 12/05/2018
ms.keywords: ID3D12Object interface,SetPrivateData method, ID3D12Object.SetPrivateData, ID3D12Object::SetPrivateData, SetPrivateData, SetPrivateData method, SetPrivateData method,ID3D12Object interface, d3d12/ID3D12Object::SetPrivateData, direct3d12.id3d12object_setprivatedata
req.header: d3d12.h
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12Object::SetPrivateData
 - d3d12/ID3D12Object::SetPrivateData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12Object.SetPrivateData
---

# ID3D12Object::SetPrivateData


## -description

Sets application-defined data to a device object and associates that data with an application-defined <b>GUID</b>.

## -parameters

### -param guid [in]

Type: <b><a href="/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50">REFGUID</a></b>

The <b>GUID</b> to associate with the data.

### -param DataSize [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The size in bytes of the data.

### -param pData [in, optional]

Type: <b>const void*</b>

A pointer to a memory block that contains the data to be stored with this device object. If <i>pData</i> is <b>NULL</b>, <i>DataSize</i> must also be 0, and any data that was previously associated with the <b>GUID</b> specified in <i>guid</i> will be destroyed.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -remarks

Rather than using the Direct3D 11 debug object naming scheme of calling <b>ID3D12Object::SetPrivateData</b> using <b>WKPDID_D3DDebugObjectName</b> with an ASCII name,
        call <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12object-setname">ID3D12Object::SetName</a> with a UNICODE name.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12object">ID3D12Object</a>