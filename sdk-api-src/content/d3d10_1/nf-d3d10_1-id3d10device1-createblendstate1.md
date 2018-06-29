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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10_1.h
api_name:
 - ID3D10Device1.CreateBlendState1
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

Type: <b>const <a href="https://msdn.microsoft.com/library/Bb694528(v=VS.85).aspx">D3D10_BLEND_DESC1</a>*</b>

Pointer to a blend-state description (see <a href="https://msdn.microsoft.com/library/Bb694528(v=VS.85).aspx">D3D10_BLEND_DESC1</a>).


### -param ppBlendState [out]

Type: <b><a href="https://msdn.microsoft.com/library/Bb694544(v=VS.85).aspx">ID3D10BlendState1</a>**</b>

Address of a pointer to the blend-state object created (see <a href="https://msdn.microsoft.com/library/Bb694544(v=VS.85).aspx">ID3D10BlendState1 Interface</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



An application can create up to 4096 unique blend-state objects. For each object created, the runtime checks to see if a previous object has the same state. If such a previous object exists, the runtime will return a pointer to previous instance instead of creating a duplicate object.

This method requires Windows Vista Service Pack 1.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb694546(v=VS.85).aspx">ID3D10Device1 Interface</a>
 

 

