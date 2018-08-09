---
UID: NF:d3d11.ID3D11DeviceContext.HSGetShader
title: ID3D11DeviceContext::HSGetShader
author: windows-sdk-content
description: Get the hull shader currently set on the device.
old-location: direct3d11\id3d11devicecontext_hsgetshader.htm
old-project: direct3d11
ms.assetid: 2ac2d88f-8c66-490e-add8-95ecaadf0147
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 86d0e4a8-a23d-ed0e-3574-68679ce095a8, HSGetShader, HSGetShader method [Direct3D 11], HSGetShader method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],HSGetShader method, ID3D11DeviceContext.HSGetShader, ID3D11DeviceContext::HSGetShader, d3d11/ID3D11DeviceContext::HSGetShader, direct3d11.id3d11devicecontext_hsgetshader
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.HSGetShader
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11DeviceContext::HSGetShader


## -description


Get the hull shader currently set on the device.


## -parameters




### -param ppHullShader [out]

Type: <b><a href="https://msdn.microsoft.com/3459f533-e2ac-4b0e-bfdd-d9dae704f418">ID3D11HullShader</a>**</b>

Address of a pointer to a hull shader (see <a href="https://msdn.microsoft.com/3459f533-e2ac-4b0e-bfdd-d9dae704f418">ID3D11HullShader</a>) to be returned by the method.


### -param ppClassInstances [out, optional]

Type: <b><a href="https://msdn.microsoft.com/70d006d2-5c47-4e8a-9a14-b5475d88ac32">ID3D11ClassInstance</a>**</b>

Pointer to an array of class instance interfaces (see <a href="https://msdn.microsoft.com/70d006d2-5c47-4e8a-9a14-b5475d88ac32">ID3D11ClassInstance</a>).


### -param pNumClassInstances [in, out, optional]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

The number of class-instance elements in the array.


## -returns



Returns nothing.




## -remarks



Any returned interfaces will have their reference count incremented by one. Applications should call IUnknown::Release on the returned interfaces when they are no longer needed to avoid memory leaks.




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

