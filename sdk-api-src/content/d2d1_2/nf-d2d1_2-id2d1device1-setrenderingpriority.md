---
UID: NF:d2d1_2.ID2D1Device1.SetRenderingPriority
title: ID2D1Device1::SetRenderingPriority (d2d1_2.h)
author: windows-sdk-content
description: Sets the priority of Direct2D rendering operations performed on any device context associated with the device.
old-location: direct2d\id2d1device1_setrenderingpriority.htm
tech.root: Direct2D
ms.assetid: 520B4D0D-8D54-4599-9BA3-A03DBF35BCFF
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID2D1Device1 interface [Direct2D],SetRenderingPriority method, ID2D1Device1.SetRenderingPriority, ID2D1Device1::SetRenderingPriority, SetRenderingPriority, SetRenderingPriority method [Direct2D], SetRenderingPriority method [Direct2D],ID2D1Device1 interface, d2d1_2/ID2D1Device1::SetRenderingPriority, direct2d.id2d1device1_setrenderingpriority
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Device1.SetRenderingPriority
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Device1::SetRenderingPriority


## -description


Sets the priority of Direct2D rendering operations performed on any device context associated with the device.


## -parameters




### -param renderingPriority

Type: <b><a href="https://msdn.microsoft.com/25DC645B-7693-468C-AE11-05F6D1B11741">D2D1_RENDERING_PRIORITY</a></b>

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



Calling this method affects the rendering priority of all device contexts associated with the device. This method can be called at any time, but is not guaranteed to take effect until the beginning of the next frame. The recommended usage is to call this method outside of <a href="https://msdn.microsoft.com/0562b286-7427-4d76-b699-a39356496a0f">BeginDraw</a> and <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">EndDraw</a> blocks. Cycling this property frequently within drawing blocks will effectively reduce the benefits of any throttling that is applied.




## -see-also




<a href="https://msdn.microsoft.com/D0CC0F2C-2BAA-4BD6-AE67-BF99458160F9">ID2D1Device1</a>
 

 

