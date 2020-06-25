---
UID: NN:winsync.IClockVector
title: IClockVector (winsync.h)
description: Represents a clock vector in a knowledge structure.
helpviewer_keywords: ["IClockVector","IClockVector interface [Windows Sync]","IClockVector interface [Windows Sync]","described","winsync.iclockvector","winsync/IClockVector"]
old-location: winsync\iclockvector.htm
tech.root: winsync
ms.assetid: 31aef38d-a6df-4645-a192-9145d3ec90ad
ms.date: 12/05/2018
ms.keywords: IClockVector, IClockVector interface [Windows Sync], IClockVector interface [Windows Sync],described, winsync.iclockvector, winsync/IClockVector
f1_keywords:
- winsync/IClockVector
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
- IClockVector
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IClockVector interface


## -description


Represents a clock vector in a knowledge structure.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IClockVector</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IClockVector</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IClockVector</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-iclockvector-getclockvectorelementcount">GetClockVectorElementCount</a>
</td>
<td align="left" width="63%">
Gets the number of elements that are contained in the clock vector.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-iclockvector-getclockvectorelements">GetClockVectorElements</a>
</td>
<td align="left" width="63%">
Returns an enumerator that iterates through the clock vector elements.


</td>
</tr>
</table> 


## -remarks



A clock vector defines the changes that are contained in a knowledge structure by using a list of <b>IClockVectorElement</b> objects. An <b>IClockVectorElement</b> object exists for each replica that has made a change that is contained in the knowledge. A change that is made by a particular replica is defined to be contained in the knowledge when the tick count for the change occurs between zero and the tick count contained in <b>IClockVectorElement</b> that tracks that replica.





## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
 

 

