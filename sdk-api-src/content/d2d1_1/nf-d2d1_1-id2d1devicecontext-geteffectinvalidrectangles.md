---
UID: NF:d2d1_1.ID2D1DeviceContext.GetEffectInvalidRectangles
title: ID2D1DeviceContext::GetEffectInvalidRectangles
author: windows-sdk-content
description: Gets the invalid rectangles that have accumulated since the last time the effect was drawn and EndDraw was then called on the device context.
old-location: direct2d\id2d1devicecontext_geteffectinvalidrectangles.htm
tech.root: direct2d
ms.assetid: D5CEFDB0-BD54-4CB9-801C-528CDA49C19C
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: GetEffectInvalidRectangles, GetEffectInvalidRectangles method [Direct2D], GetEffectInvalidRectangles method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],GetEffectInvalidRectangles method, ID2D1DeviceContext.GetEffectInvalidRectangles, ID2D1DeviceContext::GetEffectInvalidRectangles, d2d1_1/ID2D1DeviceContext::GetEffectInvalidRectangles, direct2d.id2d1devicecontext_geteffectinvalidrectangles
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1_1.h
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
req.lib: 
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1DeviceContext.GetEffectInvalidRectangles
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext::GetEffectInvalidRectangles


## -description


Gets the invalid rectangles that have accumulated since the last time the effect was drawn and <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">EndDraw</a> was then called on the device context.


## -parameters




### -param effect [in]

Type: <b><a href="https://msdn.microsoft.com/e90d1830-c356-48f1-ac7b-1d94c8c26569">ID2D1Effect</a>*</b>

The effect to get the invalid rectangles from.


### -param rectangles

TBD


### -param rectanglesCount [in]

Type: <b>UINT32</b>

The number of rectangles to get.


#### - [out]

Type: <b><a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a>*</b>

An array of <a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a> structures.  You must allocate this to the correct size.  You can get the count of the invalid rectangles using the <a href="https://msdn.microsoft.com/C0B70DA1-C9BF-47AC-BF3E-2A741DACD2E8">GetEffectInvalidRectangleCount</a> method.


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




<div class="alert"><b>Note</b>  Direct2D does not automatically use these invalid rectangles to reduce the region of an effect that is rendered.</div>
<div> </div>


You can use the <a href="https://msdn.microsoft.com/3EB22E7B-69B4-4936-B8ED-093EA1EA1759">InvalidateEffectInputRectangle</a> method to specify invalidated rectangles for Direct2D to propagate through an effect graph.

If multiple invalid rectangles are requested, the rectangles that this method returns may overlap. When this is the case, the rectangle count might be lower than the count that <a href="https://msdn.microsoft.com/C0B70DA1-C9BF-47AC-BF3E-2A741DACD2E8">GetEffectInvalidRectangleCount</a>.




## -see-also




<a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>
 

 

