---
UID: NF:d3d12.ID3D12Object.SetName
title: ID3D12Object::SetName (d3d12.h)
description: Associates a name with the device object. This name is for use in debug diagnostics and tools.
helpviewer_keywords: ["ID3D12Object interface","SetName method","ID3D12Object.SetName","ID3D12Object::SetName","SetName","SetName method","SetName method","ID3D12Object interface","d3d12/ID3D12Object::SetName","direct3d12.id3d12object_setname"]
old-location: direct3d12\id3d12object_setname.htm
tech.root: direct3d12
ms.assetid: A1DEEB16-BF75-4391-ADF0-AC22EECBC71A
ms.date: 12/05/2018
ms.keywords: ID3D12Object interface,SetName method, ID3D12Object.SetName, ID3D12Object::SetName, SetName, SetName method, SetName method,ID3D12Object interface, d3d12/ID3D12Object::SetName, direct3d12.id3d12object_setname
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
 - ID3D12Object::SetName
 - d3d12/ID3D12Object::SetName
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
 - ID3D12Object.SetName
---

# ID3D12Object::SetName


## -description

Associates a name with the device object.
          This name is for use in debug diagnostics and tools.

## -parameters

### -param Name [in]

Type: <b>LPCWSTR</b>

A <b>NULL</b>-terminated <b>UNICODE</b> string that contains the name to associate with the device object.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -remarks

This method takes UNICODE names.

Note that this is simply a convenience wrapper around [ID3D12Object::SetPrivateData](nf-d3d12-id3d12object-setprivatedata.md) with **WKPDID_D3DDebugObjectNameW**.
Therefore names which are set with `SetName` can be retrieved with [ID3D12Object::GetPrivateData](nf-d3d12-id3d12object-getprivatedata.md) with the same GUID.
Additionally, D3D12 supports narrow strings for names, using the **WKPDID_D3DDebugObjectName** GUID directly instead.

## -see-also

<a href="/windows/desktop/direct3d12/directx-12-programming-environment-set-up">Direct3D 12 Programming Environment Setup</a>



<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12object">ID3D12Object</a>