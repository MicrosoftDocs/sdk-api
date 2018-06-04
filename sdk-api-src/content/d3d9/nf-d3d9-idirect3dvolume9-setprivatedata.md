---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IDirect3DVolume9::SetPrivateData


## -description


Associates data with the volume that is intended for use by the application, not by Direct3D.


## -parameters




### -param refguid [in]

Type: <b><a href="http://go.microsoft.com/?linkid=9742306">REFGUID</a></b>

Reference to the globally unique identifier that identifies the private data to set.


### -param pData [in]

Type: <b>const void*</b>

Pointer to a buffer that contains the data to associate with the volume. 


### -param SizeOfData [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Size of the buffer at pData in bytes. 


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
The data at pData is a pointer to an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. SizeOfData must be set to the size of a pointer to an <b>IUnknown</b> interface, sizeof(IUnknown*). Direct3D automatically calls <b>IUnknown</b> through pData and IUnknown when the private data is destroyed. Private data will be destroyed by a subsequent call to <b>IDirect3DVolume9::SetPrivateData</b> with the same GUID, a subsequent call to <a href="https://msdn.microsoft.com/d4e075e0-2cd7-4160-97d6-fd8c1a932529">IDirect3DVolume9::FreePrivateData</a>, or when the <a href="https://msdn.microsoft.com/af321e4f-aaff-4285-bdac-9aab5c1dc5d8">IDirect3D9</a> object is released. For more information, see Remarks.

</td>
</tr>
</table>
 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL, E_OUTOFMEMORY.




## -remarks



Direct3D does not manage the memory at pData. If this buffer was dynamically allocated, it is the calling application's responsibility to free the memory.

Data is passed by value, and multiple sets of data can be associated with a single volume.




## -see-also




<a href="https://msdn.microsoft.com/b157d2d1-5813-43a1-ac3a-000b13b1bb62">IDirect3DVolume9</a>



<a href="https://msdn.microsoft.com/d4e075e0-2cd7-4160-97d6-fd8c1a932529">IDirect3DVolume9::FreePrivateData</a>



<a href="https://msdn.microsoft.com/73f37211-b6e6-4007-8767-6f68fa026cb5">IDirect3DVolume9::GetPrivateData</a>
 

 

