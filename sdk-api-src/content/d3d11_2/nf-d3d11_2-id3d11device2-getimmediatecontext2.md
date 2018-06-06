---
UID: NF:d3d11_2.ID3D11Device2.GetImmediateContext2
title: ID3D11Device2::GetImmediateContext2
author: windows-sdk-content
description: Gets an immediate context, which can play back command lists.
old-location: direct3d11\id3d11device2_getimmediatecontext2.htm
old-project: direct3d11
ms.assetid: 3DCA642D-7992-4C1E-8AD2-CA0099188A46
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: GetImmediateContext2, GetImmediateContext2 method [Direct3D 11], GetImmediateContext2 method [Direct3D 11],ID3D11Device2 interface, ID3D11Device2 interface [Direct3D 11],GetImmediateContext2 method, ID3D11Device2.GetImmediateContext2, ID3D11Device2::GetImmediateContext2, d3d11_2/ID3D11Device2::GetImmediateContext2, direct3d11.id3d11device2_getimmediatecontext2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps | UWP apps]
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
req.typenames: D3D11_TILE_RANGE_FLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Device2.GetImmediateContext2
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11Device2::GetImmediateContext2


## -description


Gets an immediate context, which can play back <a href="https://msdn.microsoft.com/4f581bc7-6c5e-4e56-b768-7f3cc5dbcb3e">command lists</a>. 


## -parameters




### -param ppImmediateContext [out]

Type: <b><a href="https://msdn.microsoft.com/8B6B6F6E-9236-4DEE-A1BA-5FE45736DFAA">ID3D11DeviceContext2</a>**</b>

Upon completion of the method, the passed pointer to an <a href="https://msdn.microsoft.com/8B6B6F6E-9236-4DEE-A1BA-5FE45736DFAA">ID3D11DeviceContext2</a> interface pointer is initialized.


## -returns



This method does not return a value.




## -remarks



The <b>GetImmediateContext2</b> method returns an <a href="https://msdn.microsoft.com/8B6B6F6E-9236-4DEE-A1BA-5FE45736DFAA">ID3D11DeviceContext2</a> object that represents an immediate context, which is used to perform rendering that you want immediately submitted to a device. For most apps, an immediate context is the primary object that is used to draw your scene.

The <b>GetImmediateContext2</b> method increments the reference count of the immediate context by one. Therefore, you must call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> on the returned interface pointer when you are done with it to avoid a memory leak.






## -see-also




<a href="https://msdn.microsoft.com/C476AA0E-4A49-4E1E-8308-FB72EAD3E30C">ID3D11Device2</a>
 

 

