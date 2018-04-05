---
UID: NE:d3d9types._D3DDEVTYPE
title: "_D3DDEVTYPE"
author: windows-driver-content
description: Defines device types.
old-location: direct3d9\D3DDEVTYPE.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3ddevtype.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: D3DDEVTYPE, D3DDEVTYPE enumeration [Direct3D 9], D3DDEVTYPE_FORCE_DWORD, D3DDEVTYPE_HAL, D3DDEVTYPE_NULLREF, D3DDEVTYPE_REF, D3DDEVTYPE_SW, LPD3DDEVTYPE, LPD3DDEVTYPE enumeration pointer [Direct3D 9], _D3DDEVTYPE, ceb38884-bf37-528a-de8c-ec261081c04e, d3d9types/D3DDEVTYPE, d3d9types/D3DDEVTYPE_FORCE_DWORD, d3d9types/D3DDEVTYPE_HAL, d3d9types/D3DDEVTYPE_NULLREF, d3d9types/D3DDEVTYPE_REF, d3d9types/D3DDEVTYPE_SW, d3d9types/LPD3DDEVTYPE, direct3d9.D3DDEVTYPE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d3d9types.h
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
req.typenames: D3DDEVTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DDEVTYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DDEVTYPE enumeration


## -description


Defines device types.


## -enum-fields




### -field D3DDEVTYPE_HAL

Hardware rasterization. Shading is done with software, hardware, or mixed transform and lighting.


### -field D3DDEVTYPE_REF

Direct3D features are implemented in software; however, the reference rasterizer does make use of special CPU instructions whenever it can.

The reference device is installed by the Windows SDK 8.0 or later and is intended as an aid in debugging for development only.


### -field D3DDEVTYPE_SW

A pluggable software device that has been registered with <a href="https://msdn.microsoft.com/6bed91d9-0304-4a66-8508-5e28ee34635b">IDirect3D9::RegisterSoftwareDevice</a>.


### -field D3DDEVTYPE_NULLREF

Initialize Direct3D on a computer that has neither hardware nor reference rasterization available, and enable resources for 3D content creation. See Remarks.


### -field D3DDEVTYPE_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used.


## -remarks



All methods of the <a href="https://msdn.microsoft.com/af321e4f-aaff-4285-bdac-9aab5c1dc5d8">IDirect3D9</a> interface that take a <b>D3DDEVTYPE</b> device type will fail if D3DDEVTYPE_NULLREF is specified. To use these methods, substitute D3DDEVTYPE_REF in the method call.

A D3DDEVTYPE_REF device should be created in D3DPOOL_SCRATCH memory, unless vertex and index buffers are required. To support vertex and index buffers, create the device in D3DPOOL_SYSTEMMEM memory.

If D3dref9.dll is installed, Direct3D will use the reference rasterizer to create a D3DDEVTYPE_REF device type, even if D3DDEVTYPE_NULLREF is specified. If D3dref9.dll is not available and D3DDEVTYPE_NULLREF is specified, Direct3D will neither render nor present the scene.




## -see-also




<a href="https://msdn.microsoft.com/7db5ef2b-6894-4113-b726-8b238bb4fb2f">D3DDEVICE_CREATION_PARAMETERS</a>



<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>



<a href="https://msdn.microsoft.com/39115099-de14-424c-95a8-c5699f5c4c65">IDirect3D9::CheckDeviceFormat</a>



<a href="https://msdn.microsoft.com/82f1f1f6-0d9b-497b-b532-0d2aabbd0314">IDirect3D9::CheckDeviceMultiSampleType</a>



<a href="https://msdn.microsoft.com/bd19079c-d0ee-4e2f-8a02-9f26c8abcb31">IDirect3D9::CheckDeviceType</a>



<a href="https://msdn.microsoft.com/22ad1d16-c1cc-4591-8311-daf6cf9924bb">IDirect3D9::CreateDevice</a>



<a href="https://msdn.microsoft.com/9ac080df-963b-4e29-b200-f74ff3bb6db8">IDirect3D9::GetDeviceCaps</a>
 

 

