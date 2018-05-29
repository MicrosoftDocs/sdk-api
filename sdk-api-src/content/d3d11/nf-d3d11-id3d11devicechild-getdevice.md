---
UID: NF:d3d11.ID3D11DeviceChild.GetDevice
title: ID3D11DeviceChild::GetDevice
author: windows-sdk-content
description: Get a pointer to the device that created this interface.
old-location: direct3d11\id3d11devicechild_getdevice.htm
old-project: direct3d11
ms.assetid: d18f43ef-4edc-47ff-b1be-1be670c2ccb2
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: 07aa3147-aab3-5e52-2809-7bddfdb31126, GetDevice, GetDevice method [Direct3D 11], GetDevice method [Direct3D 11],ID3D11DeviceChild interface, ID3D11DeviceChild interface [Direct3D 11],GetDevice method, ID3D11DeviceChild.GetDevice, ID3D11DeviceChild::GetDevice, d3d11/ID3D11DeviceChild::GetDevice, direct3d11.id3d11devicechild_getdevice
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
-	ID3D11DeviceChild.GetDevice
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11DeviceChild::GetDevice


## -description


Get a pointer to the device that created this interface.


## -parameters




### -param ppDevice [out]

Type: <b><a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>**</b>

Address of a pointer to a device (see <a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>).


## -returns



Returns nothing.




## -remarks



Any returned interfaces will have their reference count incremented by one, so be sure to call ::release() on the returned pointer(s) before they are freed or else you will have a memory leak.




## -see-also




<a href="https://msdn.microsoft.com/bed17239-0358-4768-8655-9a1d92f25a2e">ID3D11DeviceChild</a>
 

 

