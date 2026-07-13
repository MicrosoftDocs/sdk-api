---
UID: NF:d3d11.ID3D11DeviceChild.GetPrivateData
title: ID3D11DeviceChild::GetPrivateData (d3d11.h)
description: Get application-defined data from a device child. (ID3D11DeviceChild.GetPrivateData)
helpviewer_keywords: ["50e61586-bdf5-0fe2-ab52-a873243bc7ff","GetPrivateData","GetPrivateData method [Direct3D 11]","GetPrivateData method [Direct3D 11]","ID3D11DeviceChild interface","ID3D11DeviceChild interface [Direct3D 11]","GetPrivateData method","ID3D11DeviceChild.GetPrivateData","ID3D11DeviceChild::GetPrivateData","d3d11/ID3D11DeviceChild::GetPrivateData","direct3d11.id3d11devicechild_getprivatedata"]
old-location: direct3d11\id3d11devicechild_getprivatedata.htm
tech.root: direct3d11
ms.assetid: 11729527-680e-4c70-a10f-278feab8362d
ms.date: 12/05/2018
ms.keywords: 50e61586-bdf5-0fe2-ab52-a873243bc7ff, GetPrivateData, GetPrivateData method [Direct3D 11], GetPrivateData method [Direct3D 11],ID3D11DeviceChild interface, ID3D11DeviceChild interface [Direct3D 11],GetPrivateData method, ID3D11DeviceChild.GetPrivateData, ID3D11DeviceChild::GetPrivateData, d3d11/ID3D11DeviceChild::GetPrivateData, direct3d11.id3d11devicechild_getprivatedata
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
 - ID3D11DeviceChild::GetPrivateData
 - d3d11/ID3D11DeviceChild::GetPrivateData
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
 - ID3D11DeviceChild.GetPrivateData
---

# ID3D11DeviceChild::GetPrivateData


## -description

Get application-defined data from a device child.

## -parameters

### -param guid [in]

Type: <b><a href="/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50">REFGUID</a></b>

Guid associated with the data.

### -param pDataSize [in, out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

A pointer to a variable that on input contains the size, in bytes, of the buffer that <i>pData</i> points to, and on output contains the size, in bytes, of the amount of data that
           <b>GetPrivateData</b> retrieved.

### -param pData [out, optional]

Type: <b>void*</b>

A pointer to a buffer that
           <b>GetPrivateData</b> fills with data from the device child if <i>pDataSize</i> points to a value that specifies a buffer large enough to hold the data.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the 
            <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

The data stored in the device child is set by calling <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicechild-setprivatedata">ID3D11DeviceChild::SetPrivateData</a>.
        
If the data returned is a pointer to an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>, or one of its derivative classes, which was previously set by **SetPrivateDataInterface**, that interface will have its reference count incremented before the private data is returned.

<b>Windows Phone 8:
        </b> This API is supported.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>
