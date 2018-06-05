---
UID: NF:d3d10.ID3D10Device.IASetInputLayout
title: ID3D10Device::IASetInputLayout
author: windows-sdk-content
description: Bind an input-layout object to the input-assembler stage.
old-location: direct3d10\id3d10device_iasetinputlayout.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_iasetinputlayout.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: 5492ac19-1f40-6d42-38a5-490e297331f0, IASetInputLayout, IASetInputLayout method [Direct3D 10], IASetInputLayout method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],IASetInputLayout method, ID3D10Device.IASetInputLayout, ID3D10Device::IASetInputLayout, d3d10/ID3D10Device::IASetInputLayout, direct3d10.id3d10device_iasetinputlayout
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
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
-	ID3D10Device.IASetInputLayout
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::IASetInputLayout


## -description


Bind an input-layout object to the <a href="https://msdn.microsoft.com/71141a5e-2d79-4b02-8370-c0cbc8618908">input-assembler stage</a>.


## -parameters




### -param pInputLayout [in]

Type: <b><a href="https://msdn.microsoft.com/0a58bfcb-8b32-4fe7-a078-0695ab0d9806">ID3D10InputLayout</a>*</b>

A pointer to the input-layout object (see <a href="https://msdn.microsoft.com/0a58bfcb-8b32-4fe7-a078-0695ab0d9806">ID3D10InputLayout</a>), which describes the input buffers that will be read by the IA stage.


## -returns



Returns nothing.




## -remarks



Input-layout objects describe how vertex buffer data is streamed into the IA pipeline stage. To create an input-layout object, call <a href="https://msdn.microsoft.com/61516e1a-f588-4dcb-9ada-9b483fe7cc99">ID3D10Device::CreateInputLayout</a>.

The method will not hold a reference to the interfaces passed in. For that reason, applications should be careful not to release an interface currently in use by the device.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

