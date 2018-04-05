---
UID: NF:d3d10.ID3D10DeviceChild.GetDevice
title: ID3D10DeviceChild::GetDevice method
author: windows-driver-content
description: Get a pointer to the device that created this interface.
old-location: direct3d10\id3d10devicechild_getdevice.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10devicechild_getdevice.htm
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: GetDevice method [Direct3D 10], GetDevice method [Direct3D 10], ID3D10DeviceChild interface, GetDevice,ID3D10DeviceChild.GetDevice, ID3D10DeviceChild, ID3D10DeviceChild interface [Direct3D 10], GetDevice method, ID3D10DeviceChild::GetDevice, a6448c63-5b6c-87fa-33e0-73a8850ca573, d3d10/ID3D10DeviceChild::GetDevice, direct3d10.id3d10devicechild_getdevice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d10.h
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
req.typenames: D3D10_USAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10.lib
-	D3D10.dll
api_name:
-	ID3D10DeviceChild.GetDevice
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10DeviceChild::GetDevice method


## -description


Get a pointer to the device that created this interface.


## -parameters




### -param ppDevice [out]

Type: <b><a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device</a>**</b>

Address of a pointer to a device (see <a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>).


## -returns



Returns nothing.




## -remarks



Any returned interfaces will have their reference count incremented by one, so be sure to call ::release() on the returned pointer(s) before they are freed or else you will have a memory leak.




## -see-also




<a href="https://msdn.microsoft.com/64eff938-e130-48be-a45f-43f6c885b588">ID3D10DeviceChild Interface</a>
 

 

