---
UID: NF:d3d10_1.ID3D10Device1.CreateBlendState1
title: ID3D10Device1::CreateBlendState1
author: windows-sdk-content
description: Create a blend-state object that encapsules blend state for the output-merger stage.
old-location: direct3d10\id3d10device1_createblendstate1.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device1_createblendstate1.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: CreateBlendState1, CreateBlendState1 method [Direct3D 10], CreateBlendState1 method [Direct3D 10],ID3D10Device1 interface, ID3D10Device1 interface [Direct3D 10],CreateBlendState1 method, ID3D10Device1.CreateBlendState1, ID3D10Device1::CreateBlendState1, b8ad390b-12a5-cfce-2558-a74e808c9358, d3d10_1/ID3D10Device1::CreateBlendState1, direct3d10.id3d10device1_createblendstate1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10_1.h
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
req.typenames: D3D10_FEATURE_LEVEL1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10_1.h
api_name:
-	ID3D10Device1.CreateBlendState1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10Device1::CreateBlendState1


## -description


Create a blend-state object that encapsules blend state for the output-merger stage.


## -parameters




### -param pBlendStateDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/1da6dc74-ff15-4707-866d-5aaf80c495f9">D3D10_BLEND_DESC1</a>*</b>

Pointer to a blend-state description (see <a href="https://msdn.microsoft.com/1da6dc74-ff15-4707-866d-5aaf80c495f9">D3D10_BLEND_DESC1</a>).


### -param ppBlendState [out]

Type: <b><a href="https://msdn.microsoft.com/acb41920-8090-4357-afe0-ba5a6644b984">ID3D10BlendState1</a>**</b>

Address of a pointer to the blend-state object created (see <a href="https://msdn.microsoft.com/acb41920-8090-4357-afe0-ba5a6644b984">ID3D10BlendState1 Interface</a>).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



An application can create up to 4096 unique blend-state objects. For each object created, the runtime checks to see if a previous object has the same state. If such a previous object exists, the runtime will return a pointer to previous instance instead of creating a duplicate object.

This method requires Windows Vista Service Pack 1.




## -see-also




<a href="https://msdn.microsoft.com/511f710d-f35e-46bf-93e0-47b6ceb5c84d">ID3D10Device1 Interface</a>
 

 

