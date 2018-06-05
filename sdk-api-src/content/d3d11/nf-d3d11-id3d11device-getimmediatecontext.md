---
UID: NF:d3d11.ID3D11Device.GetImmediateContext
title: ID3D11Device::GetImmediateContext
author: windows-sdk-content
description: Gets an immediate context, which can play back command lists.
old-location: direct3d11\id3d11device_getimmediatecontext.htm
old-project: direct3d11
ms.assetid: 0349f0b8-7696-4d72-bed4-d39b9ac90f6c
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: 2f9e01b9-f7a8-4cdb-2811-bbd0a44df05f, GetImmediateContext, GetImmediateContext method [Direct3D 11], GetImmediateContext method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],GetImmediateContext method, ID3D11Device.GetImmediateContext, ID3D11Device::GetImmediateContext, d3d11/ID3D11Device::GetImmediateContext, direct3d11.id3d11device_getimmediatecontext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D11.lib
-	D3D11.dll
api_name:
-	ID3D11Device.GetImmediateContext
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11Device::GetImmediateContext


## -description


Gets an immediate context, which can play back command lists.


## -parameters




### -param ppImmediateContext [out]

Type: <b><a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>**</b>

Upon completion of the method, the passed pointer to an <a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a> interface pointer is initialized.


## -returns



This method does not return a value.




## -remarks



The <b>GetImmediateContext</b> method returns an <a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a> object that represents an immediate context which is used to perform rendering that you want immediately submitted to a device. For most applications, an immediate context is the primary object that is used to draw your scene.

The <b>GetImmediateContext</b> method increments the reference count of the immediate context by one. Therefore, you must call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> on the returned interface pointer when you are done with it to avoid a memory leak.






## -see-also




<a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>
 

 

