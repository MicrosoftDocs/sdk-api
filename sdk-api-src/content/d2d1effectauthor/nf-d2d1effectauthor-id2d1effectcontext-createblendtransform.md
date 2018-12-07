---
UID: NF:d2d1effectauthor.ID2D1EffectContext.CreateBlendTransform
title: ID2D1EffectContext::CreateBlendTransform
author: windows-sdk-content
description: This creates a blend transform that can be inserted into a transform graph.
old-location: direct2d\id2d1contextinternal_createblendtransform.htm
tech.root: direct2d
ms.assetid: 23B8D1A5-05F4-4056-BFA8-8D9C89FE0492
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateBlendTransform, CreateBlendTransform method [Direct2D], CreateBlendTransform method [Direct2D],ID2D1EffectContext interface, ID2D1EffectContext interface [Direct2D],CreateBlendTransform method, ID2D1EffectContext.CreateBlendTransform, ID2D1EffectContext::CreateBlendTransform, d2d1effectauthor/ID2D1EffectContext::CreateBlendTransform, direct2d.id2d1contextinternal_createblendtransform
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
req.lib: D2D1.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2D1.lib
 - D2D1.dll
api_name:
 - ID2D1EffectContext.CreateBlendTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1EffectContext::CreateBlendTransform


## -description


This creates a blend transform that can be inserted into a transform graph. 




## -parameters




### -param numInputs

Type: <b>UINT32</b>

The number of inputs to the blend transform.


### -param blendDescription [in]

Type: <b>const <a href="https://msdn.microsoft.com/5f4c7248-9303-4451-92f1-4b230efd627a">D2D1_BLEND_DESCRIPTION</a>*</b>

Describes the blend transform that is to be created.


### -param transform [out]

Type: <b><a href="https://msdn.microsoft.com/0DC46758-6005-4A33-9539-9C95CF8CFB6A">ID2D1BlendTransform</a>**</b>

The returned blend transform.


## -returns



Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
<td>E_OUTOFMEMORY</td>
<td>Direct2D could not allocate sufficient memory to complete the call.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>An invalid parameter was passed to the returning function.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6BE6DF90-C5B7-4377-9DBF-804AB1C91FEE">ID2D1EffectContext</a>
 

 

