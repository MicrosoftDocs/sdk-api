---
UID: NF:d3d10.ID3D10Device.IAGetInputLayout
title: ID3D10Device::IAGetInputLayout
author: windows-sdk-content
description: Get a pointer to the input-layout object that is bound to the input-assembler stage.
old-location: direct3d10\id3d10device_iagetinputlayout.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_iagetinputlayout.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IAGetInputLayout, IAGetInputLayout method [Direct3D 10], IAGetInputLayout method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],IAGetInputLayout method, ID3D10Device.IAGetInputLayout, ID3D10Device::IAGetInputLayout, d3d10/ID3D10Device::IAGetInputLayout, direct3d10.id3d10device_iagetinputlayout, fc7e34a5-1fc3-6283-98db-681a4f1138cf
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10.h
req.include-header: 
req.redist: 
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.h
api_name:
 - ID3D10Device.IAGetInputLayout
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10Device::IAGetInputLayout


## -description


Get a pointer to the input-layout object that is bound to the <a href="https://msdn.microsoft.com/71141a5e-2d79-4b02-8370-c0cbc8618908">input-assembler stage</a>.


## -parameters




### -param ppInputLayout [out]

Type: <b><a href="https://msdn.microsoft.com/0a58bfcb-8b32-4fe7-a078-0695ab0d9806">ID3D10InputLayout</a>**</b>

A pointer to the input-layout object (see <a href="https://msdn.microsoft.com/0a58bfcb-8b32-4fe7-a078-0695ab0d9806">ID3D10InputLayout</a>), which describes the input buffers that will be read by the IA stage.


## -returns



Returns nothing.




## -remarks



For information about creating an input-layout object, see <a href="https://msdn.microsoft.com/84c0ca29-2356-4b7f-98ee-ff1758edc540">Creating the Input-Layout Object</a>.

Any returned interfaces will have their reference count incremented by one. Applications should call <a href="http://msdn.microsoft.com/en-us/library/ms682317(VS.85).aspx">IUnknown::Release</a> on the returned interfaces when they are no longer needed to avoid memory leaks.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

