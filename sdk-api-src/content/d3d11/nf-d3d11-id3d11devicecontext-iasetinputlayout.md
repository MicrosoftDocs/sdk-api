---
UID: NF:d3d11.ID3D11DeviceContext.IASetInputLayout
title: ID3D11DeviceContext::IASetInputLayout
author: windows-sdk-content
description: Bind an input-layout object to the input-assembler stage.
old-location: direct3d11\id3d11devicecontext_iasetinputlayout.htm
old-project: direct3d11
ms.assetid: 54562ece-db8d-4e31-bde2-36391792e259
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: IASetInputLayout, IASetInputLayout method [Direct3D 11], IASetInputLayout method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],IASetInputLayout method, ID3D11DeviceContext.IASetInputLayout, ID3D11DeviceContext::IASetInputLayout, d3d11/ID3D11DeviceContext::IASetInputLayout, direct3d11.id3d11devicecontext_iasetinputlayout, f3e6f365-7707-18d4-cb39-e78b1f31d4c8
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
 - ID3D11DeviceContext.IASetInputLayout
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
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
 

 

