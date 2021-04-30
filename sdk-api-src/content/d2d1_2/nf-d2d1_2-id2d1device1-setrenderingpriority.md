---
UID: NF:d2d1_2.ID2D1Device1.SetRenderingPriority
title: ID2D1Device1::SetRenderingPriority (d2d1_2.h)
description: Sets the priority of Direct2D rendering operations performed on any device context associated with the device.
helpviewer_keywords: ["ID2D1Device1 interface [Direct2D]","SetRenderingPriority method","ID2D1Device1.SetRenderingPriority","ID2D1Device1::SetRenderingPriority","SetRenderingPriority","SetRenderingPriority method [Direct2D]","SetRenderingPriority method [Direct2D]","ID2D1Device1 interface","d2d1_2/ID2D1Device1::SetRenderingPriority","direct2d.id2d1device1_setrenderingpriority"]
old-location: direct2d\id2d1device1_setrenderingpriority.htm
tech.root: Direct2D
ms.assetid: 520B4D0D-8D54-4599-9BA3-A03DBF35BCFF
ms.date: 12/05/2018
ms.keywords: ID2D1Device1 interface [Direct2D],SetRenderingPriority method, ID2D1Device1.SetRenderingPriority, ID2D1Device1::SetRenderingPriority, SetRenderingPriority, SetRenderingPriority method [Direct2D], SetRenderingPriority method [Direct2D],ID2D1Device1 interface, d2d1_2/ID2D1Device1::SetRenderingPriority, direct2d.id2d1device1_setrenderingpriority
req.header: d2d1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Device1::SetRenderingPriority
 - d2d1_2/ID2D1Device1::SetRenderingPriority
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Device1.SetRenderingPriority
---

# ID2D1Device1::SetRenderingPriority


## -description

Sets the priority of Direct2D rendering operations performed on any device context associated with the device.

## -parameters

### -param renderingPriority

Type: <b><a href="/windows/desktop/api/d2d1_2/ne-d2d1_2-d2d1_rendering_priority">D2D1_RENDERING_PRIORITY</a></b>

The desired rendering priority for the device and associated contexts.

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

Calling this method affects the rendering priority of all device contexts associated with the device. This method can be called at any time, but is not guaranteed to take effect until the beginning of the next frame. The recommended usage is to call this method outside of <a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw">BeginDraw</a> and <a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">EndDraw</a> blocks. Cycling this property frequently within drawing blocks will effectively reduce the benefits of any throttling that is applied.

## -see-also

<a href="/windows/desktop/api/d2d1_2/nn-d2d1_2-id2d1device1">ID2D1Device1</a>