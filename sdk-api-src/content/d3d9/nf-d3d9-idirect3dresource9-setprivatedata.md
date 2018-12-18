---
UID: NF:d3d9.IDirect3DResource9.SetPrivateData
title: IDirect3DResource9::SetPrivateData
author: windows-sdk-content
description: Associates data with the resource that is intended for use by the application, not by Direct3D. Data is passed by value, and multiple sets of data can be associated with a single resource.
old-location: direct3d9\idirect3dresource9__setprivatedata.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dresource9__setprivatedata.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 0424643d-f9ce-ea1d-5f27-9017b5eed4ea, IDirect3DResource9 interface [Direct3D 9],SetPrivateData method, IDirect3DResource9.SetPrivateData, IDirect3DResource9::SetPrivateData, SetPrivateData, SetPrivateData method [Direct3D 9], SetPrivateData method [Direct3D 9],IDirect3DResource9 interface, d3d9helper/IDirect3DResource9::SetPrivateData, direct3d9.idirect3dresource9__setprivatedata
ms.topic: method
req.header: d3d9.h
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DResource9::SetPrivateData


## -description


Associates data with the resource that is intended for use by the application, not by Direct3D. Data is passed by value, and multiple sets of data can be associated with a single resource.


## -parameters




### -param refguid [in]

Type: <b><a href="http://go.microsoft.com/?linkid=9742306">REFGUID</a></b>

Reference to the globally unique identifier that identifies the private data to set.


### -param pData [in]

Type: <b>const void*</b>

Pointer to a buffer that contains the data to be associated with the resource. 


### -param SizeOfData [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Size of the buffer at pData, in bytes. 


### -param Flags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

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
The data at pData is a pointer to an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. 
SizeOfData must be set to the size of a pointer to IUnknown, that is, sizeof(IUnknown*). Direct3D automatically callsIUnknown through pData when the private data is destroyed. Private data will be destroyed by a subsequent call to <b>IDirect3DResource9::SetPrivateData</b> with the same GUID, a subsequent call to <a href="https://msdn.microsoft.com/en-us/library/Bb205879(v=VS.85).aspx">IDirect3DResource9::FreePrivateData</a>, or when the <a href="https://msdn.microsoft.com/en-us/library/Bb174300(v=VS.85).aspx">IDirect3D9</a> object is released. For more information, see Remarks.

</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL, E_OUTOFMEMORY.




## -remarks



Direct3D does not manage the memory at pData. If this buffer was dynamically allocated, it is the calling application's responsibility to free the memory.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205878(v=VS.85).aspx">IDirect3DResource9</a>
 

 

