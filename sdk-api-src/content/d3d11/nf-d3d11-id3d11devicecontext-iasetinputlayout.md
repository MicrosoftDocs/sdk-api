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

# ID3D11DeviceContext::IASetInputLayout


## -description


Bind an input-layout object to the input-assembler stage.


## -parameters




### -param pInputLayout [in, optional]

Type: <b><a href="https://msdn.microsoft.com/df83fcdc-ff1b-4901-9f1f-15eb2fe5241c">ID3D11InputLayout</a>*</b>

A pointer to the input-layout object (see <a href="https://msdn.microsoft.com/df83fcdc-ff1b-4901-9f1f-15eb2fe5241c">ID3D11InputLayout</a>), which describes the input buffers that will be read by the IA stage.


## -returns



Returns nothing.




## -remarks



Input-layout objects describe how vertex buffer data is streamed into the IA pipeline stage. To create an input-layout object, call <a href="https://msdn.microsoft.com/fe233b7b-3729-428a-8611-e98ea4c5af35">ID3D11Device::CreateInputLayout</a>.


      The method will hold a reference to the interfaces passed in.
      This differs from the device state behavior in Direct3D 10.




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

