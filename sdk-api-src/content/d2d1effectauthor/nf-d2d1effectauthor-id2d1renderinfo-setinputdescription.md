---
UID: NF:d2d1effectauthor.ID2D1RenderInfo.SetInputDescription
title: ID2D1RenderInfo::SetInputDescription
author: windows-sdk-content
description: Sets how a specific input to the transform should be handled by the renderer in terms of sampling.
old-location: direct2d\id2d1renderinfo_setinputdescription.htm
tech.root: direct2d
ms.assetid: 31571676-7030-4FBB-BDED-3CE3BA7E7CE6
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: ID2D1RenderInfo interface [Direct2D],SetInputDescription method, ID2D1RenderInfo.SetInputDescription, ID2D1RenderInfo::SetInputDescription, SetInputDescription, SetInputDescription method [Direct2D], SetInputDescription method [Direct2D],ID2D1RenderInfo interface, d2d1effectauthor/ID2D1RenderInfo::SetInputDescription, direct2d.id2d1renderinfo_setinputdescription
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1effectauthor.h
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
req.lib: D2d1.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1.lib
 - d2d1.dll
api_name:
 - ID2D1RenderInfo.SetInputDescription
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderInfo::SetInputDescription


## -description


Sets how a specific input to the transform should be handled by the renderer in terms of sampling.


## -parameters




### -param inputIndex

TBD


### -param inputDescription

Type: <b><a href="https://msdn.microsoft.com/ba900ef8-a71a-4aac-a884-38917b78b8df">D2D1_INPUT_DESCRIPTION</a></b>

The description of the input to be applied to the transform.


#### - index

Type: <b>UINT32</b>

The index of the input that will have the input description applied.


## -returns



Type: <b>HRESULT</b>

The method returns an HRESULT. Possible values include, but are not limited to, those in the following table.


<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>No error occurred.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>An invalid parameter was passed to the returning function.</td>
</tr>
</table>
 






## -remarks



The input description must be matched correctly by the effect shader code.




## -see-also




<a href="https://msdn.microsoft.com/a2a4b4fd-685d-4068-b1f5-609e6ab024e2">D2D1_BUFFER_PRECISION</a>



<a href="https://msdn.microsoft.com/78129b15-a770-49c0-b58b-8cb850f80006">D2D1_CHANNEL_DEPTH</a>



<a href="https://msdn.microsoft.com/6a066126-89d0-4372-bc01-6b6fa1d65440">ID2D1DeviceContext::SetRenderingControls</a>



<a href="https://msdn.microsoft.com/26FB6D27-7EE0-43DA-A575-D9FF77846A16">ID2D1RenderInfo</a>
 

 

