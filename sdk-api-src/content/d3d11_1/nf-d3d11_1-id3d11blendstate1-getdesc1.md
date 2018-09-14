---
UID: NF:d3d11_1.ID3D11BlendState1.GetDesc1
title: ID3D11BlendState1::GetDesc1
author: windows-sdk-content
description: Gets the description for blending state that you used to create the blend-state object.
old-location: direct3d11\id3d11blendstate1_getdesc1.htm
tech.root: direct3d11
ms.assetid: BD256EB6-2FDD-4BBA-99E7-D7AA2CBDD629
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetDesc1, GetDesc1 method [Direct3D 11], GetDesc1 method [Direct3D 11],ID3D11BlendState1 interface, ID3D11BlendState1 interface [Direct3D 11],GetDesc1 method, ID3D11BlendState1.GetDesc1, ID3D11BlendState1::GetDesc1, d3d11_1/ID3D11BlendState1::GetDesc1, direct3d11.id3d11blendstate1_getdesc1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - ID3D11BlendState1.GetDesc1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11BlendState1::GetDesc1


## -description


Gets the description for blending state that you used to create the blend-state object.


## -parameters




### -param pDesc [out]

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Hh404435(v=VS.85).aspx">D3D11_BLEND_DESC1</a> structure that receives a description of the blend state. This blend state can specify logical operations as well as blending operations.


## -returns



Returns nothing.




## -remarks



You use the description for blending state in a call to the <a href="https://msdn.microsoft.com/en-us/library/Hh404577(v=VS.85).aspx">ID3D11Device1::CreateBlendState1</a> method to create the blend-state object.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh404571(v=VS.85).aspx">ID3D11BlendState1</a>
 

 

