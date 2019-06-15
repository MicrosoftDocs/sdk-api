---
UID: NN:d2d1_1.ID2D1PrintControl
title: ID2D1PrintControl (d2d1_1.h)
author: windows-sdk-content
description: Converts Direct2D primitives stored in an ID2D1CommandList into a fixed page representation. The print sub-system then consumes the primitives.
old-location: direct2d\id2d1printcontrol.htm
tech.root: Direct2D
ms.assetid: 0E8D8218-0671-44A2-AD6E-13BB0B4EB66C
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID2D1PrintControl, ID2D1PrintControl interface [Direct2D], ID2D1PrintControl interface [Direct2D],described, d2d1_1/ID2D1PrintControl, direct2d.id2d1printcontrol
ms.topic: interface
f1_keywords: ["d2d1_1/ID2D1PrintControl"]
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
ms.custom: 19H1
---

# ID2D1PrintControl interface


## -description


Converts <a href="https://docs.microsoft.com/windows/desktop/Direct2D/direct2d-portal">Direct2D</a> primitives stored in an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandlist">ID2D1CommandList</a> into a fixed page representation.  The print sub-system then consumes the primitives.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1PrintControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID2D1PrintControl</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1printcontrol-addpage">AddPage</a>
</td>
<td align="left" width="63%">
Converts Direct2D primitives in the passed-in command list into a fixed page representation for use  by the print subsystem. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1printcontrol-close">Close</a>
</td>
<td align="left" width="63%">
Passes all remaining resources to the print sub-system, then clean up and close the current print job. 

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Direct2D/printing-and-command-lists">Printing and Command Lists</a>
 

 

