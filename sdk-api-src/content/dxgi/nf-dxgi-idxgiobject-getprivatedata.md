---
UID: NF:dxgi.IDXGIObject.GetPrivateData
title: IDXGIObject::GetPrivateData
author: windows-sdk-content
description: Get a pointer to the object's data.
old-location: direct3ddxgi\idxgiobject_getprivatedata.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiobject_getprivatedata.htm
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: 86763938-a2bf-a817-2ffc-645427783675, GetPrivateData, GetPrivateData method [DXGI], GetPrivateData method [DXGI],IDXGIObject interface, IDXGIObject interface [DXGI],GetPrivateData method, IDXGIObject.GetPrivateData, IDXGIObject::GetPrivateData, direct3ddxgi.idxgiobject_getprivatedata, dxgi/IDXGIObject::GetPrivateData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dxgi.h
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
req.lib: DXGI.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGIObject.GetPrivateData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIObject::GetPrivateData


## -description


Get a pointer to the object's data.


## -parameters




### -param Name [in]

Type: <b><a href="http://go.microsoft.com/?linkid=9742306">REFGUID</a></b>

A GUID identifying the data.


### -param pDataSize [in, out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

The size of the data.


### -param pData [out]

Type: <b>void*</b>

Pointer to the data.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>.




## -remarks



If the data returned is a pointer to an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>, or one of its derivative classes, previously set by <a href="https://msdn.microsoft.com/7b64aa3a-ccb3-4aed-a37b-58e4bd77ed8c">IDXGIObject::SetPrivateDataInterface</a>, you must call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">::Release()</a> on the pointer before the pointer is freed to decrement the reference count.

You can pass <b>GUID_DeviceType</b> in the <i>Name</i> parameter of <b>GetPrivateData</b> to retrieve the device type from the display adapter object (<a href="https://msdn.microsoft.com/02fc6b37-bd8f-4889-96cc-91064d23c9d0">IDXGIAdapter</a>, <a href="https://msdn.microsoft.com/003d5a10-e978-481f-8ca6-9e5ab69bfec0">IDXGIAdapter1</a>, <a href="https://msdn.microsoft.com/9AAD133C-CE40-498B-827F-2B35C7C15B8C">IDXGIAdapter2</a>). 

<p class="proch"><img alt="" src="../common/wedge.gif"/><b>To get the type of device on which the display adapter was created</b>

<ol>
<li>Call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a> on the <a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a> or <a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device</a> object to retrieve the <a href="https://msdn.microsoft.com/83b24b82-9044-4c99-8d50-63f1e8aef8db">IDXGIDevice</a> object.</li>
<li>Call <a href="https://msdn.microsoft.com/7e7f7494-445e-4bf1-8b94-fc40b7d9b887">GetParent</a> on the <a href="https://msdn.microsoft.com/83b24b82-9044-4c99-8d50-63f1e8aef8db">IDXGIDevice</a> object to retrieve the <a href="https://msdn.microsoft.com/02fc6b37-bd8f-4889-96cc-91064d23c9d0">IDXGIAdapter</a> object.</li>
<li>Call <b>GetPrivateData</b> on the <a href="https://msdn.microsoft.com/02fc6b37-bd8f-4889-96cc-91064d23c9d0">IDXGIAdapter</a> object with <b>GUID_DeviceType</b> to retrieve the type of device on which the display adapter was created. <i>pData</i> will point to a value from the driver-type enumeration (for example, a value from <a href="https://msdn.microsoft.com/ceeec7d6-4bdc-488c-80a8-6c5e11986d6a">D3D_DRIVER_TYPE</a>).</li>
</ol>
On Windows 7 or earlier, this type is either a value from <a href="https://msdn.microsoft.com/0dc66bd9-4e88-460f-a05d-b78347a29cad">D3D10_DRIVER_TYPE</a> or <a href="https://msdn.microsoft.com/ceeec7d6-4bdc-488c-80a8-6c5e11986d6a">D3D_DRIVER_TYPE</a> depending on which kind of device was created. On Windows 8, this type is always a value from <b>D3D_DRIVER_TYPE</b>. Don't use <a href="https://msdn.microsoft.com/fd34c22f-a8fa-4012-be4c-e251b951261f">IDXGIObject::SetPrivateData</a> with <b>GUID_DeviceType</b> because the behavior when doing so is undefined.




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/baf1dc5a-ae7e-4bc5-affa-11ed16091625">IDXGIObject</a>
 

 

