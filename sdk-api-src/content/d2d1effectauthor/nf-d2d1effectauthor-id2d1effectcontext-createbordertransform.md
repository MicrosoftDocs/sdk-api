---
UID: NF:d2d1effectauthor.ID2D1EffectContext.CreateBorderTransform
title: ID2D1EffectContext::CreateBorderTransform
author: windows-sdk-content
description: Creates a transform that extends its input infinitely in every direction based on the passed in extend mode.
old-location: direct2d\id2d1contextinternal_createbordertransform.htm
tech.root: direct2d
ms.assetid: E1FC2BF9-7287-4F9B-BDCF-3CD6EC8B849D
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: CreateBorderTransform, CreateBorderTransform method [Direct2D], CreateBorderTransform method [Direct2D],ID2D1EffectContext interface, ID2D1EffectContext interface [Direct2D],CreateBorderTransform method, ID2D1EffectContext.CreateBorderTransform, ID2D1EffectContext::CreateBorderTransform, d2d1effectauthor/ID2D1EffectContext::CreateBorderTransform, direct2d.id2d1contextinternal_createbordertransform
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
 - ID2D1EffectContext.CreateBorderTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1EffectContext::CreateBorderTransform


## -description


Creates a transform that extends its input infinitely in every direction based on the passed in extend mode.


## -parameters




### -param extendModeX

Type: <b><a href="https://msdn.microsoft.com/6b6e1fe1-d43a-46cf-904d-5266b9bd6bf4">D2D1_EXTEND_MODE</a></b>

The extend mode in the X-axis direction.


### -param extendModeY

Type: <b><a href="https://msdn.microsoft.com/6b6e1fe1-d43a-46cf-904d-5266b9bd6bf4">D2D1_EXTEND_MODE</a></b>

The extend mode in the Y-axis direction.


### -param transform [out]

Type: <b><a href="https://msdn.microsoft.com/79C4E7E8-6042-4ECA-BD95-069760CF2A55">ID2D1BorderTransform</a>**</b>

The returned transform.


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
 

 

