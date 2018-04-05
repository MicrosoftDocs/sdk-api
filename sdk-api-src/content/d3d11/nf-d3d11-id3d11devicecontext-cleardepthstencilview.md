---
UID: NF:d3d11.ID3D11DeviceContext.ClearDepthStencilView
title: ID3D11DeviceContext::ClearDepthStencilView method
author: windows-driver-content
description: Clears the depth-stencil resource.
old-location: direct3d11\id3d11devicecontext_cleardepthstencilview.htm
old-project: direct3d11
ms.assetid: 1e2269cf-edef-466e-be59-95dc644c7a0c
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: ClearDepthStencilView method [Direct3D 11], ClearDepthStencilView method [Direct3D 11], ID3D11DeviceContext interface, ClearDepthStencilView,ID3D11DeviceContext.ClearDepthStencilView, ID3D11DeviceContext, ID3D11DeviceContext interface [Direct3D 11], ClearDepthStencilView method, ID3D11DeviceContext::ClearDepthStencilView, d3d11/ID3D11DeviceContext::ClearDepthStencilView, d4e31518-5c9c-aa0c-b817-a09a4886e3f2, direct3d11.id3d11devicecontext_cleardepthstencilview
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
-	ID3D11DeviceContext.ClearDepthStencilView
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11DeviceContext::ClearDepthStencilView method


## -description


Clears the depth-stencil resource.


## -parameters




### -param pDepthStencilView [in]

Type: <b><a href="https://msdn.microsoft.com/10be1fd1-8700-4c0a-b447-d3c2569f8e81">ID3D11DepthStencilView</a>*</b>

Pointer to the depth stencil to be cleared.


### -param ClearFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Identify the type of data to clear (see <a href="https://msdn.microsoft.com/6da515f3-d71d-4b59-b2ea-cacdf78fcb42">D3D11_CLEAR_FLAG</a>).


### -param Depth [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

Clear the depth buffer with this value. This value will be clamped between 0 and 1.


### -param Stencil [in]

Type: <b>UINT8</b>

Clear the stencil buffer with this value.


## -returns



Returns nothing.




## -remarks



<table>
<tr>
<td>
Differences between Direct3D 9 and Direct3D 11/10:

Unlike Direct3D 9, the full extent of the resource view is always cleared. Viewport and scissor settings are not applied.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

