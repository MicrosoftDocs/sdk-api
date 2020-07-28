---
UID: NN:winsync.IRangeException
title: IRangeException (winsync.h)
description: Represents an item ID range to exclude from a knowledge object.
helpviewer_keywords: ["IRangeException","IRangeException interface [Windows Sync]","IRangeException interface [Windows Sync]","described","winsync.irangeexception","winsync/IRangeException"]
old-location: winsync\irangeexception.htm
tech.root: winsync
ms.assetid: 7eea9fe0-80e7-43a9-a797-df12d4d809dc
ms.date: 12/05/2018
ms.keywords: IRangeException, IRangeException interface [Windows Sync], IRangeException interface [Windows Sync],described, winsync.irangeexception, winsync/IRangeException
f1_keywords:
- winsync/IRangeException
dev_langs:
- c++
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- winsync.h
api_name:
- IRangeException
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRangeException interface


## -description


Represents an item ID range to exclude from a knowledge object.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRangeException</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRangeException</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRangeException</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-irangeexception-getclockvector">GetClockVector</a>
</td>
<td align="left" width="63%">
Gets the clock vector that is associated with this exception.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-irangeexception-getclosedrangeend">GetClosedRangeEnd</a>
</td>
<td align="left" width="63%">
Gets the upper bound of the range of item IDs to exclude.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-irangeexception-getclosedrangestart">GetClosedRangeStart</a>
</td>
<td align="left" width="63%">
Gets the lower bound of the range of item IDs to exclude.


</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
 

 

