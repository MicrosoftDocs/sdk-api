---
UID: NN:d2d1_1.ID2D1PrintControl
title: ID2D1PrintControl (d2d1_1.h)
author: windows-sdk-content
description: Converts Direct2D primitives stored in an ID2D1CommandList into a fixed page representation. The print sub-system then consumes the primitives.
old-location: direct2d\id2d1printcontrol.htm
tech.root: Direct2D
ms.assetid: 0E8D8218-0671-44A2-AD6E-13BB0B4EB66C
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID2D1PrintControl, ID2D1PrintControl interface [Direct2D], ID2D1PrintControl interface [Direct2D],described, d2d1_1/ID2D1PrintControl, direct2d.id2d1printcontrol
ms.topic: interface
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
 - ID2D1PrintControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1PrintControl interface


## -description


Converts <a href="https://msdn.microsoft.com/03b3b91c-9751-4f8d-af24-85067f06930b">Direct2D</a> primitives stored in an <a href="https://msdn.microsoft.com/30b89f53-d20b-4070-abcd-ef95813130d1">ID2D1CommandList</a> into a fixed page representation.  The print sub-system then consumes the primitives.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1PrintControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID2D1PrintControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1PrintControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6B157EE8-36C8-4054-9975-3D3B82B3D013">AddPage</a>
</td>
<td align="left" width="63%">
Converts Direct2D primitives in the passed-in command list into a fixed page representation for use  by the print subsystem. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ADCA373-C461-4737-A292-AF29977B148C">Close</a>
</td>
<td align="left" width="63%">
Passes all remaining resources to the print sub-system, then clean up and close the current print job. 

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/C51ACCDE-B205-4F79-A2FD-D112BAAD1616">Printing and Command Lists</a>
 

 

