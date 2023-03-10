---
UID: NF:d3d9helper.IDirect3DResource9.SetPrivateData
title: IDirect3DResource9::SetPrivateData (d3d9helper.h)
description: The IDirect3DResource9::SetPrivateData method (d3d9helper.h) associates data with the resource that is intended for use by the application, not by Direct3D.
helpviewer_keywords: ["0424643d-f9ce-ea1d-5f27-9017b5eed4ea","IDirect3DResource9 interface [Direct3D 9]","SetPrivateData method","IDirect3DResource9.SetPrivateData","IDirect3DResource9::SetPrivateData","SetPrivateData","SetPrivateData method [Direct3D 9]","SetPrivateData method [Direct3D 9]","IDirect3DResource9 interface","d3d9helper/IDirect3DResource9::SetPrivateData","direct3d9.idirect3dresource9__setprivatedata"]
old-location: direct3d9\idirect3dresource9__setprivatedata.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dresource9__setprivatedata.htm
ms.date: 08/11/2022
ms.keywords: 0424643d-f9ce-ea1d-5f27-9017b5eed4ea, IDirect3DResource9 interface [Direct3D 9],SetPrivateData method, IDirect3DResource9.SetPrivateData, IDirect3DResource9::SetPrivateData, SetPrivateData, SetPrivateData method [Direct3D 9], SetPrivateData method [Direct3D 9],IDirect3DResource9 interface, d3d9helper/IDirect3DResource9::SetPrivateData, direct3d9.idirect3dresource9__setprivatedata
req.header: d3d9helper.h
req.include-header: D3D9.h
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3DResource9::SetPrivateData
 - d3d9helper/IDirect3DResource9::SetPrivateData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DResource9.SetPrivateData
---

# IDirect3DResource9::SetPrivateData


## -description

Associates data with the resource that is intended for use by the application, not by Direct3D. Data is passed by value, and multiple sets of data can be associated with a single resource.

## -parameters

### -param refguid [in]

Type: <b><a href="/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50">REFGUID</a></b>

Reference to the globally unique identifier that identifies the private data to set.

### -param pData [in]

Type: <b>const void*</b>

Pointer to a buffer that contains the data to be associated with the resource.

### -param SizeOfData [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Size of the buffer at pData, in bytes.

### -param Flags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Value that describes the type of data being passed, or indicates to the application that the data should be invalidated when the resource changes. 



<table>
<tr>
<th>Item</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="_none_"></a><a id="_NONE_"></a>(none)

</td>
<td width="60%">
If no flags are specified, Direct3D allocates memory to hold the data within the buffer and copies the data into the new buffer. The buffer allocated by Direct3D is automatically freed, as appropriate.

</td>
</tr>
<tr>
<td width="40%">
<a id="D3DSPD_IUNKNOWN"></a><a id="d3dspd_iunknown"></a>D3DSPD_IUNKNOWN

</td>
<td width="60%">
The data at pData is a pointer to an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. 
SizeOfData must be set to the size of a pointer to IUnknown, that is, sizeof(IUnknown*). Direct3D automatically callsIUnknown through pData when the private data is destroyed. Private data will be destroyed by a subsequent call to <b>IDirect3DResource9::SetPrivateData</b> with the same GUID, a subsequent call to <a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dresource9-freeprivatedata">IDirect3DResource9::FreePrivateData</a>, or when the <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3d9">IDirect3D9</a> object is released. For more information, see Remarks.

</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL, E_OUTOFMEMORY.

## -remarks

Direct3D does not manage the memory at pData. If this buffer was dynamically allocated, it is the calling application's responsibility to free the memory.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dresource9">IDirect3DResource9</a>
