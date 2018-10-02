---
UID: NF:d2d1_1.ID2D1DeviceContext.InvalidateEffectInputRectangle
title: ID2D1DeviceContext::InvalidateEffectInputRectangle
author: windows-sdk-content
description: This indicates that a portion of an effect's input is invalid. This method can be called many times.
old-location: direct2d\id2d1devicecontext_invalidateeffectinputrectangle.htm
tech.root: direct2d
ms.assetid: 3EB22E7B-69B4-4936-B8ED-093EA1EA1759
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: ID2D1DeviceContext interface [Direct2D],InvalidateEffectInputRectangle method, ID2D1DeviceContext.InvalidateEffectInputRectangle, ID2D1DeviceContext::InvalidateEffectInputRectangle, InvalidateEffectInputRectangle, InvalidateEffectInputRectangle method [Direct2D], InvalidateEffectInputRectangle method [Direct2D],ID2D1DeviceContext interface, d2d1_1/ID2D1DeviceContext::InvalidateEffectInputRectangle, direct2d.id2d1devicecontext_invalidateeffectinputrectangle
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
 - ID2D1DeviceContext.InvalidateEffectInputRectangle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext::InvalidateEffectInputRectangle


## -description


This indicates that a portion of an effect's input is invalid. This method can
     be called many times.

You can use this method to propagate invalid rectangles through an effect graph. You can query Direct2D using the <a href="https://msdn.microsoft.com/D5CEFDB0-BD54-4CB9-801C-528CDA49C19C">GetEffectInvalidRectangles</a> method.
<div class="alert"><b>Note</b>  Direct2D does not automatically use these invalid rectangles to reduce the region of an effect that is rendered.</div><div> </div>You can also use this method to invalidate caches that have accumulated while rendering effects that have the <b>D2D1_PROPERTY_CACHED</b> property set to true.


## -parameters




### -param effect [in]

Type: <b><a href="https://msdn.microsoft.com/e90d1830-c356-48f1-ac7b-1d94c8c26569">ID2D1Effect</a>*</b>

The effect to invalidate.


### -param input

Type: <b>UINT32</b>

The input index.


### -param inputRectangle [in]

Type: <b>const <a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a>*</b>

The rect to invalidate.


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




<a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>
 

 

