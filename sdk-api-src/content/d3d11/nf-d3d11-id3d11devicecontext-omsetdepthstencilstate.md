---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ID3D11DeviceContext::OMSetDepthStencilState


## -description


Sets the depth-stencil state of the output-merger stage.


## -parameters




### -param pDepthStencilState [in, optional]

Type: <b><a href="https://msdn.microsoft.com/cac22076-2ba6-4ab1-918e-8c9a7773acf6">ID3D11DepthStencilState</a>*</b>

Pointer to a depth-stencil state interface (see <a href="https://msdn.microsoft.com/cac22076-2ba6-4ab1-918e-8c9a7773acf6">ID3D11DepthStencilState</a>) to bind to the device. Set this to <b>NULL</b> to use the default state listed in <a href="https://msdn.microsoft.com/5e136ca8-8655-4c75-9bc0-bcf3a7af930a">D3D11_DEPTH_STENCIL_DESC</a>.


### -param StencilRef [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Reference value to perform against when doing a depth-stencil test. See remarks.


## -returns



Returns nothing.




## -remarks



To create a depth-stencil state interface, call <a href="https://msdn.microsoft.com/7577604c-922c-408c-8eab-2361ebda17df">ID3D11Device::CreateDepthStencilState</a>.


      The method will hold a reference to the interfaces passed in.
      This differs from the device state behavior in Direct3D 10.




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

