---
UID: NN:d2d1_1.ID2D1Device
title: ID2D1Device (d2d1_1.h)
description: Represents a resource domain whose objects and device contexts can be used together.
helpviewer_keywords: ["ID2D1Device","ID2D1Device interface [Direct2D]","ID2D1Device interface [Direct2D]","described","d2d1_1/ID2D1Device","direct2d.id2d1device"]
old-location: direct2d\id2d1device.htm
tech.root: Direct2D
ms.assetid: 21f77c38-c115-4fdf-b294-570577a29201
ms.date: 12/05/2018
ms.keywords: ID2D1Device, ID2D1Device interface [Direct2D], ID2D1Device interface [Direct2D],described, d2d1_1/ID2D1Device, direct2d.id2d1device
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Device
 - d2d1_1/ID2D1Device
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
 - ID2D1Device
---

# ID2D1Device interface


## -description

Represents a resource domain whose objects and device contexts can be used together.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1Device</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1resource">ID2D1Resource</a>. <b>ID2D1Device</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1Device</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1device-clearresources">ClearResources</a>
</td>
<td align="left" width="63%">
Clears all of the rendering resources used by Direct2D. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1device-createdevicecontext">CreateDeviceContext</a>
</td>
<td align="left" width="63%">
Creates a new device context from a Direct2D device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-createprintcontrol">CreatePrintControl</a>
</td>
<td align="left" width="63%">Overloaded. Creates an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1printcontrol">ID2D1PrintControl</a> object that converts <a href="https://docs.microsoft.com/windows/desktop/Direct2D/direct2d-portal">Direct2D</a> primitives stored in <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandlist">ID2D1CommandList</a> into a fixed page representation.  The print sub-system then consumes the primitives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1device-getmaximumtexturememory">GetMaximumTextureMemory</a>
</td>
<td align="left" width="63%">
Sets the maximum amount of texture memory Direct2D accumulates before it purges the image caches and cached texture allocations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1device-setmaximumtexturememory">SetMaximumTextureMemory</a>
</td>
<td align="left" width="63%">
Sets the maximum amount of texture memory Direct2D accumulates before it purges the image caches and cached texture allocations.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevice">D2D1CreateDevice</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1factory1-createdevice">ID2D1Factory1::CreateDevice</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1resource">ID2D1Resource</a>

