---
UID: NF:d3d12.ID3D12Object.SetPrivateDataInterface
title: ID3D12Object::SetPrivateDataInterface (d3d12.h)
description: Associates an IUnknown-derived interface with the device object and associates that interface with an application-defined GUID.
helpviewer_keywords: ["ID3D12Object interface","SetPrivateDataInterface method","ID3D12Object.SetPrivateDataInterface","ID3D12Object::SetPrivateDataInterface","SetPrivateDataInterface","SetPrivateDataInterface method","SetPrivateDataInterface method","ID3D12Object interface","d3d12/ID3D12Object::SetPrivateDataInterface","direct3d12.id3d12object_setprivatedatainterface"]
old-location: direct3d12\id3d12object_setprivatedatainterface.htm
tech.root: direct3d12
ms.assetid: B03B9420-7E85-4C1A-858C-37B20E4D9B52
ms.date: 12/05/2018
ms.keywords: ID3D12Object interface,SetPrivateDataInterface method, ID3D12Object.SetPrivateDataInterface, ID3D12Object::SetPrivateDataInterface, SetPrivateDataInterface, SetPrivateDataInterface method, SetPrivateDataInterface method,ID3D12Object interface, d3d12/ID3D12Object::SetPrivateDataInterface, direct3d12.id3d12object_setprivatedatainterface
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
 - ID3D12Object::SetPrivateDataInterface
 - d3d12/ID3D12Object::SetPrivateDataInterface
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
 - ID3D12Object.SetPrivateDataInterface
---

# ID3D12Object::SetPrivateDataInterface


## -description

Associates an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>-derived interface with the device object and associates that interface with an application-defined <b>GUID</b>.

## -parameters

### -param guid [in]

Type: <b><a href="/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50">REFGUID</a></b>

The <b>GUID</b> to associate with the interface.

### -param pData [in, optional]

Type: <b>const <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>-derived interface to be associated with the device object. Its reference count is incremented when set, and its reference count is decremented when either the ID3D12Object is destroyed or when the data is overwritten by calling SetPrivateData or SetPrivateDataInterface with the same GUID.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12object">ID3D12Object</a>
