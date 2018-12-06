---
UID: NF:d2d1_1.ID2D1Factory1.CreateDevice
title: ID2D1Factory1::CreateDevice
author: windows-sdk-content
description: Creates a ID2D1Device object.
old-location: direct2d\id2d1factory1_createdevice.htm
tech.root: direct2d
ms.assetid: d16569c1-e366-45fe-9079-ed9eb894547b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateDevice, CreateDevice method [Direct2D], CreateDevice method [Direct2D],ID2D1Factory1 interface, ID2D1Factory1 interface [Direct2D],CreateDevice method, ID2D1Factory1.CreateDevice, ID2D1Factory1::CreateDevice, d2d1_1/ID2D1Factory1::CreateDevice, direct2d.id2d1factory1_createdevice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Factory1.CreateDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Factory1::CreateDevice


## -description


Creates a <a href="https://msdn.microsoft.com/21f77c38-c115-4fdf-b294-570577a29201">ID2D1Device</a> object.


## -parameters




### -param dxgiDevice [in]

Type: <b><a href="https://msdn.microsoft.com/83b24b82-9044-4c99-8d50-63f1e8aef8db">IDXGIDevice</a>*</b>

The <a href="https://msdn.microsoft.com/83b24b82-9044-4c99-8d50-63f1e8aef8db">IDXGIDevice</a> object used when creating  the <a href="https://msdn.microsoft.com/21f77c38-c115-4fdf-b294-570577a29201">ID2D1Device</a>. 


### -param d2dDevice [out]

Type: <b><a href="https://msdn.microsoft.com/21f77c38-c115-4fdf-b294-570577a29201">ID2D1Device</a>**</b>

The requested <a href="https://msdn.microsoft.com/21f77c38-c115-4fdf-b294-570577a29201">ID2D1Device</a> object.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.


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
<td>An invalid parameter was passed to the returning function.</td>
</tr>
<tr>
<td>D3DERR_OUTOFVIDEOMEMORY</td>
<td>Direct3D does not have enough display memory to perform the operation.</td>
</tr>
</table>
 






## -remarks



The <a href="https://msdn.microsoft.com/03b3b91c-9751-4f8d-af24-85067f06930b">Direct2D</a> device defines a resource domain in which a set of Direct2D objects and Direct2D device contexts can be used together.  Each call to <a href="https://msdn.microsoft.com/5ed3ec21-b609-41b6-9568-6ede460bc395">CreateDevice</a> returns a unique <a href="https://msdn.microsoft.com/21f77c38-c115-4fdf-b294-570577a29201">ID2D1Device</a> object, even if you pass the same <a href="https://msdn.microsoft.com/83b24b82-9044-4c99-8d50-63f1e8aef8db">IDXGIDevice</a> multiple times.




## -see-also




<a href="https://msdn.microsoft.com/21f77c38-c115-4fdf-b294-570577a29201">ID2D1Device</a>



<a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>



<a href="https://msdn.microsoft.com/8c8664cb-d6be-41e0-8415-d60dcd46132a">ID2D1DeviceContext::GetDevice</a>



<a href="https://msdn.microsoft.com/8221c3b4-e331-403c-9406-ee8d3e103825">ID2D1Factory1</a>
 

 

