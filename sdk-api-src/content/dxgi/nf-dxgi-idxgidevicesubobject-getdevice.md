---
UID: NF:dxgi.IDXGIDeviceSubObject.GetDevice
title: IDXGIDeviceSubObject::GetDevice
author: windows-sdk-content
description: Retrieves the device.
old-location: direct3ddxgi\idxgidevicesubobject_getdevice.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgidevicesubobject_getdevice.htm
ms.author: windowssdkdev
ms.date: 07/02/2018
ms.keywords: GetDevice, GetDevice method [DXGI], GetDevice method [DXGI],IDXGIDeviceSubObject interface, IDXGIDeviceSubObject interface [DXGI],GetDevice method, IDXGIDeviceSubObject.GetDevice, IDXGIDeviceSubObject::GetDevice, b3dce65b-334c-0973-c391-77df6912fc77, direct3ddxgi.idxgidevicesubobject_getdevice, dxgi/IDXGIDeviceSubObject::GetDevice
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DXGI_SWAP_EFFECT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGIDeviceSubObject.GetDevice
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIDeviceSubObject::GetDevice


## -description


Retrieves the device.


## -parameters




### -param riid [in]

Type: <b>REFIID</b>

The reference id for the device.


### -param ppDevice [out]

Type: <b>void**</b>

The address of a pointer to the device.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

A code that indicates success or failure (see <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>).




## -remarks



The type of interface that is returned can be any interface published by the device. For example, it could be an IDXGIDevice * called pDevice, and therefore the REFIID would be obtained by calling __uuidof(pDevice).




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/f2f3da88-76e9-4721-bc02-b3b82b7794b8">IDXGIDeviceSubObject</a>
 

 

