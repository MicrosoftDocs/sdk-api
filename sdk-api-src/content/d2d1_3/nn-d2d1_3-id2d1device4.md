---
UID: NN:d2d1_3.ID2D1Device4
title: ID2D1Device4
author: windows-sdk-content
description: Represents a resource domain whose objects and device contexts can be used together. This interface performs all the same functions as the ID2D1Device3 interface. It also enables the creation of ID2D1DeviceContext4 objects.
old-location: direct2d\id2d1device4.htm
tech.root: direct2d
ms.assetid: B91E4E63-5FB5-4470-A3B9-F94008EAE4E9
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: ID2D1Device4, ID2D1Device4 interface [Direct2D], ID2D1Device4 interface [Direct2D],described, d2d1_3/ID2D1Device4, direct2d.id2d1device4
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
 - ID2D1Device4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Device4 interface


## -description


Represents a resource domain whose objects and device contexts can be used together.
          This interface performs all the same functions as the <a href="https://msdn.microsoft.com/60CB6308-85BE-424B-9950-1C8617D08A09">ID2D1Device3</a> interface.
          It also enables the creation of <a href="https://msdn.microsoft.com/59E1F73B-BAD9-4826-BF5B-435E760CC546">ID2D1DeviceContext4</a> objects.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1Device4</b> interface inherits from <a href="https://msdn.microsoft.com/60CB6308-85BE-424B-9950-1C8617D08A09">ID2D1Device3</a>. <b>ID2D1Device4</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1Device4</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06F097C4-E417-48EA-A480-62E96C4A1CE6">CreateDeviceContext</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/59E1F73B-BAD9-4826-BF5B-435E760CC546">ID2D1DeviceContext4</a> from this Direct2D device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D2863860-D2CE-4658-AD06-F29B827947EE">GetMaximumColorGlyphCacheMemory</a>
</td>
<td align="left" width="63%">
Gets the maximum capacity of the color glyph cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/477386A0-0EED-489A-BBFD-8371153D5BA1">SetMaximumColorGlyphCacheMemory</a>
</td>
<td align="left" width="63%">
Sets the maximum capacity of the color glyph cache. 

</td>
</tr>
</table> 

