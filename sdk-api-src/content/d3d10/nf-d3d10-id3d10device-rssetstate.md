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

# ID3D10Device::RSSetState


## -description


Set the <a href="https://msdn.microsoft.com/ae4bb4c4-35a8-43c3-bfa5-f57b44bc367e">rasterizer state</a> for the <a href="https://msdn.microsoft.com/efd3f819-7c63-4e1a-9923-8e7198354ec6">rasterizer stage</a> of the pipeline.


## -parameters




### -param pRasterizerState [in]

Type: <b><a href="https://msdn.microsoft.com/c365ab8a-085b-4706-b355-c4319673bdb7">ID3D10RasterizerState</a>*</b>

Pointer to a rasterizer-state interface (see <a href="https://msdn.microsoft.com/c365ab8a-085b-4706-b355-c4319673bdb7">ID3D10RasterizerState</a>) to bind to the pipeline.


## -returns



Returns nothing.




## -remarks



To create a rasterizer state interface, call <a href="https://msdn.microsoft.com/bd304e42-e4f6-4bc4-baf0-b4c8287e3351">ID3D10Device::CreateRasterizerState</a>. For more details on setting up the rasterizer state, see <a href="https://msdn.microsoft.com/d78c3845-76fd-4bd7-a603-bb1d8c66ac49">Set Rasterizer State</a>.

The method will not hold a reference to the interfaces passed in. For that reason, applications should be careful not to release an interface currently in use by the device.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

