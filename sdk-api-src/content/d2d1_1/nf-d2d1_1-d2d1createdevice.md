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

# D2D1CreateDevice function


## -description


Creates a new Direct2D device associated with the provided DXGI device. 


## -parameters




### -param dxgiDevice [in]

The DXGI device the Direct2D device is associated with.


### -param creationProperties [in, optional]

The properties to apply to the Direct2D device.


### -param d2dDevice [out]

When this function returns, contains the address of a pointer to a Direct2D device.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>No error occurred.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>Direct2D could not allocate sufficient memory to complete the call.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>An invalid value was passed to the method.</td>
</tr>
</table>
 




## -remarks



This function will also create a new <a href="https://msdn.microsoft.com/8221c3b4-e331-403c-9406-ee8d3e103825">ID2D1Factory1</a> that can be retrieved through <a href="https://msdn.microsoft.com/93afc187-d1ef-46f8-98b0-efe31345ae98">ID2D1Resource::GetFactory</a>.

If the creation properties are not specified, then <i>d2dDevice</i> will inherit its threading mode from <i>dxgiDevice</i> and debug tracing will not be enabled.




## -see-also




<a href="https://msdn.microsoft.com/8c0a685a-8f33-4072-a715-bb423cb44f03">D2D1CreateFactory</a>



<a href="https://msdn.microsoft.com/657439fe-dc17-42af-9e2c-2f3cb769a5a3">D2D1_CREATION_PROPERTIES</a>



<a href="https://msdn.microsoft.com/21f77c38-c115-4fdf-b294-570577a29201">ID2D1Device</a>



<a href="https://msdn.microsoft.com/cef6115c-98e8-49e6-b419-271b43ce2938">ID2D1Factory</a>



<a href="https://msdn.microsoft.com/93afc187-d1ef-46f8-98b0-efe31345ae98">ID2D1Resource::GetFactory</a>
 

 

