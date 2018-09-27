---
UID: NF:d2d1effectauthor.ID2D1EffectContext.CreateOffsetTransform
title: ID2D1EffectContext::CreateOffsetTransform
author: windows-sdk-content
description: Creates and returns an offset transform.
old-location: direct2d\id2d1contextinternal_createoffsettransform.htm
tech.root: direct2d
ms.assetid: A0A479F7-CB2C-4A9A-B482-2383A3A1A841
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: CreateOffsetTransform, CreateOffsetTransform method [Direct2D], CreateOffsetTransform method [Direct2D],ID2D1EffectContext interface, ID2D1EffectContext interface [Direct2D],CreateOffsetTransform method, ID2D1EffectContext.CreateOffsetTransform, ID2D1EffectContext::CreateOffsetTransform, d2d1effectauthor/ID2D1EffectContext::CreateOffsetTransform, direct2d.id2d1contextinternal_createoffsettransform
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
 - ID2D1EffectContext.CreateOffsetTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1EffectContext::CreateOffsetTransform


## -description


Creates and returns an offset transform.


## -parameters




### -param offset

Type: <b><a href="https://msdn.microsoft.com/B782EDE3-54A2-4FCA-8E9C-C472950A5509">D2D1_POINT_2L</a></b>

The offset amount.


### -param transform [out]

Type: <b><a href="https://msdn.microsoft.com/0809C0FC-2F7B-49D8-A695-AD451C9BD17F">ID2D1OffsetTransform</a>**</b>

When this method returns, contains the address of a pointer to an offset transform object.


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
 




## -remarks



An offset transform is used to offset an input bitmap without having to insert a rendering pass. An offset transform is automatically inserted by an Affine transform if the transform evaluates to a pixel-aligned transform.




## -see-also




<a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>



<a href="https://msdn.microsoft.com/6BE6DF90-C5B7-4377-9DBF-804AB1C91FEE">ID2D1EffectContext</a>
 

 

