---
UID: NN:d2d1_2.ID2D1DeviceContext1
title: ID2D1DeviceContext1
author: windows-sdk-content
description: Enables creation and drawing of geometry realization objects.
old-location: direct2d\id2d1devicecontext1.htm
tech.root: Direct2D
ms.assetid: E08FDAE4-05D3-472C-9AD9-228BAF989F1D
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID2D1DeviceContext1, ID2D1DeviceContext1 interface [Direct2D], ID2D1DeviceContext1 interface [Direct2D],described, d2d1_2/ID2D1DeviceContext1, direct2d.id2d1devicecontext1
ms.topic: interface
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.lib
 - D2d1.dll
api_name:
 - ID2D1DeviceContext1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext1 interface


## -description


Enables creation and drawing of geometry realization objects.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1DeviceContext1</b> interface inherits from <a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>. <b>ID2D1DeviceContext1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1DeviceContext1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7628592C-4D42-42C1-948A-DAB4E7D6C2D4">CreateFilledGeometryRealization</a>
</td>
<td align="left" width="63%">
Creates a device-dependent representation of the fill of the geometry that can be subsequently rendered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/455EE223-4CEA-4FBA-8885-B0BA6B465C05">CreateStrokedGeometryRealization</a>
</td>
<td align="left" width="63%">
Creates a device-dependent representation of the stroke of a geometry that can be subsequently rendered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BA4FB8E7-E59A-42BD-86BB-8048267A26AA">DrawGeometryRealization</a>
</td>
<td align="left" width="63%">
Renders a given geometry realization to the target with the specified brush.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>
 

 

