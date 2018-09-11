---
UID: NF:d3d11.ID3D11DeviceContext.IAGetInputLayout
title: ID3D11DeviceContext::IAGetInputLayout
author: windows-sdk-content
description: Get a pointer to the input-layout object that is bound to the input-assembler stage.
old-location: direct3d11\id3d11devicecontext_iagetinputlayout.htm
tech.root: direct3d11
ms.assetid: b3d07e01-405e-4973-956f-85a08b720aaa
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 833fde64-5672-81f0-24a0-876e6fb4fc29, IAGetInputLayout, IAGetInputLayout method [Direct3D 11], IAGetInputLayout method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],IAGetInputLayout method, ID3D11DeviceContext.IAGetInputLayout, ID3D11DeviceContext::IAGetInputLayout, d3d11/ID3D11DeviceContext::IAGetInputLayout, direct3d11.id3d11devicecontext_iagetinputlayout
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.IAGetInputLayout
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11DeviceContext::IAGetInputLayout


## -description


Get a pointer to the input-layout object that is bound to the input-assembler stage.


## -parameters




### -param ppInputLayout [out]

Type: <b><a href="https://msdn.microsoft.com/df83fcdc-ff1b-4901-9f1f-15eb2fe5241c">ID3D11InputLayout</a>**</b>

A pointer to the input-layout object (see <a href="https://msdn.microsoft.com/df83fcdc-ff1b-4901-9f1f-15eb2fe5241c">ID3D11InputLayout</a>), which describes the input buffers that will be read by the IA stage.


## -returns



Returns nothing.




## -remarks



For information about creating an input-layout object, see Creating the Input-Layout Object.

Any returned interfaces will have their reference count incremented by one. Applications should call IUnknown::Release on the returned interfaces when they are no longer needed to avoid memory leaks.




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

