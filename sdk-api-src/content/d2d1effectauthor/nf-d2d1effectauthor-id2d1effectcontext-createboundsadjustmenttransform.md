---
UID: NF:d2d1effectauthor.ID2D1EffectContext.CreateBoundsAdjustmentTransform
title: ID2D1EffectContext::CreateBoundsAdjustmentTransform
author: windows-sdk-content
description: Creates and returns a bounds adjustment transform.
old-location: direct2d\id2d1effectcontext_createboundsadjustment.htm
tech.root: Direct2D
ms.assetid: 6B6820E5-792F-447C-81C9-493FA572F61A
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CreateBoundsAdjustmentTransform, CreateBoundsAdjustmentTransform method [Direct2D], CreateBoundsAdjustmentTransform method [Direct2D],ID2D1EffectContext interface, ID2D1EffectContext interface [Direct2D],CreateBoundsAdjustmentTransform method, ID2D1EffectContext.CreateBoundsAdjustmentTransform, ID2D1EffectContext::CreateBoundsAdjustmentTransform, d2d1effectauthor/ID2D1EffectContext::CreateBoundsAdjustmentTransform, direct2d.id2d1effectcontext_createboundsadjustment
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
 - ID2D1EffectContext.CreateBoundsAdjustmentTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1EffectContext::CreateBoundsAdjustmentTransform


## -description


Creates and returns a bounds adjustment  transform.


## -parameters




### -param outputRectangle [in]

Type: <b>const <a href="https://msdn.microsoft.com/655EBC1A-199E-40A2-A4C2-9622AFAEE0B5">D2D1_RECT_L</a>*</b>

The initial output rectangle for the bounds adjustment transform.


### -param transform [out]

Type: <b><a href="https://msdn.microsoft.com/40482670-2989-47B2-9558-FF017C8A2FBB">ID2D1BoundsAdjustmentTransform</a>**</b>

The returned bounds adjustment transform.


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



A support transform can be used for two different reasons.

<ul>
<li>To indicate that a region of its input image is already transparent black. This can increase efficiency for rendering bitmaps. <div class="alert"><b>Note</b>  If the indicated region does NOT contain only transparent black pixels, then rendering results are undefined.</div>
<div> </div>
</li>
<li>To increase the size of the input image. The expanded area will be treated as transparent black
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/6BE6DF90-C5B7-4377-9DBF-804AB1C91FEE">ID2D1EffectContext</a>
 

 

