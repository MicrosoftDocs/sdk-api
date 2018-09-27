---
UID: NN:d2d1_3.ID2D1ColorContext1
title: ID2D1ColorContext1
author: windows-sdk-content
description: Represents a color context to be used with the Color Management Effect.
old-location: direct2d\id2d1colorcontext1.htm
tech.root: direct2d
ms.assetid: 77C8730B-C753-48E7-89C1-FBE28E687704
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ID2D1ColorContext1, ID2D1ColorContext1 interface [Direct2D], ID2D1ColorContext1 interface [Direct2D],described, d2d1_3/ID2D1ColorContext1, direct2d.id2d1colorcontext1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d2d1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - ID2D1ColorContext1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1ColorContext1 interface


## -description


Represents a color context to be used with the Color Management Effect.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1ColorContext1</b> interface inherits from <a href="https://msdn.microsoft.com/acdda11e-eb3f-4258-b24e-daa3b7a23fd6">ID2D1ColorContext</a>. <b>ID2D1ColorContext1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1ColorContext1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9A9E4EE4-943B-4332-B9F1-269CF629A8FA">GetColorContextType</a>
</td>
<td align="left" width="63%">
Retrieves the color context type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DDDF1277-D1E6-49AF-8F2F-F1B18BC2DB7D">GetDXGIColorSpace</a>
</td>
<td align="left" width="63%">
Retrieves the DXGI color space of this context. Returns DXGI_COLOR_SPACE_CUSTOM when color context type is ICC.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AD80B59A-AF86-4BCB-9360-D49E4337E020">GetSimpleColorProfile</a>
</td>
<td align="left" width="63%">
Retrieves a set simple color profile.

</td>
</tr>
</table> 

