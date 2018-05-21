---
UID: NF:dxgi.IDXGIObject.SetPrivateDataInterface
title: IDXGIObject::SetPrivateDataInterface
author: windows-driver-content
description: Set an interface in the object's private data.
old-location: direct3ddxgi\idxgiobject_setprivatedatainterface.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiobject_setprivatedatainterface.htm
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: 37e6a4f2-50a5-efad-af10-20e8f1d053e2, IDXGIObject interface [DXGI],SetPrivateDataInterface method, IDXGIObject.SetPrivateDataInterface, IDXGIObject::SetPrivateDataInterface, SetPrivateDataInterface, SetPrivateDataInterface method [DXGI], SetPrivateDataInterface method [DXGI],IDXGIObject interface, direct3ddxgi.idxgiobject_setprivatedatainterface, dxgi/IDXGIObject::SetPrivateDataInterface
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
req.typenames: DXGI_SWAP_EFFECT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	DXGI.lib
-	DXGI.dll
api_name:
-	IDXGIObject.SetPrivateDataInterface
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIObject::SetPrivateDataInterface


## -description


Set an interface in the object's private data.


## -parameters




### -param Name [in]

Type: <b><a href="http://go.microsoft.com/?linkid=9742306">REFGUID</a></b>

A GUID identifying the interface.


### -param pUnknown [in]

Type: <b>const <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

The interface to set.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>.




## -remarks



This API associates an interface pointer with the object.

When the interface is set its reference count is incremented. When the data are overwritten (by calling SPD or SPDI with the same GUID) or the object is destroyed, ::Release() is called and the interface's reference count is decremented.




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/baf1dc5a-ae7e-4bc5-affa-11ed16091625">IDXGIObject</a>
 

 

