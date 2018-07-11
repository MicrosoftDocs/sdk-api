---
UID: NF:d3d9.IDirect3DDevice9.GetSoftwareVertexProcessing
title: IDirect3DDevice9::GetSoftwareVertexProcessing
author: windows-sdk-content
description: Gets the vertex processing (hardware or software) mode.
old-location: direct3d9\idirect3ddevice9__getsoftwarevertexprocessing.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getsoftwarevertexprocessing.htm
ms.author: windowssdkdev
ms.date: 04/11/2018
ms.keywords: 17efcf07-7357-cfad-13db-c6391873f457, GetSoftwareVertexProcessing, GetSoftwareVertexProcessing method [Direct3D 9], GetSoftwareVertexProcessing method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetSoftwareVertexProcessing method, IDirect3DDevice9.GetSoftwareVertexProcessing, IDirect3DDevice9::GetSoftwareVertexProcessing, d3d9helper/IDirect3DDevice9::GetSoftwareVertexProcessing, direct3d9.idirect3ddevice9__getsoftwarevertexprocessing
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d9.h
req.include-header: D3D9.h
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
req.typenames: D3D12_SIGNATURE_PARAMETER_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DDevice9.GetSoftwareVertexProcessing
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::GetSoftwareVertexProcessing


## -description


Gets the vertex processing (hardware or software) mode.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns <b>TRUE</b> if software vertex processing is set. Otherwise, it returns <b>FALSE</b>.




## -remarks



An application can create a mixed-mode device to use both the software vertex processing and the hardware vertex processing. To switch between the two vertex processing modes in DirectX 8.x, use <a href="https://msdn.microsoft.com/65738aae-aa90-48c5-8c9c-1927d1c92c54">IDirect3DDevice9::SetRenderState</a> with the render state D3DRS_SOFTWAREVERTEXPROCESSING and the appropriate BOOL argument. The drawback of the render state approach was the difficulty in defining the semantics for state blocks. Applications and the runtime had to do extra work and be careful while recording and playing back state blocks.

In Direct3D 9, use <a href="https://msdn.microsoft.com/05e67ec5-98f8-47c4-b5b7-aabb974db88a">IDirect3DDevice9::SetSoftwareVertexProcessing</a> instead. This new API is not recorded by StateBlocks.

 Also refer to the notes for the <a href="https://msdn.microsoft.com/91387a2d-3927-4285-a09b-9ce247e6bfdd">D3DCREATE</a> constants.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>
 

 

