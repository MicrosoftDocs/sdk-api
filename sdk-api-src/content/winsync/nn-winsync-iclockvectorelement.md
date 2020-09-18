---
UID: NN:winsync.IClockVectorElement
title: IClockVectorElement (winsync.h)
description: Represents a clock vector element of a knowledge structure.
helpviewer_keywords: ["IClockVectorElement","IClockVectorElement interface [Windows Sync]","IClockVectorElement interface [Windows Sync]","described","winsync.iclockvectorelement","winsync/IClockVectorElement"]
old-location: winsync\iclockvectorelement.htm
tech.root: winsync
ms.assetid: cae24ef0-5b31-48c2-99bd-9e0954ec3b37
ms.date: 12/05/2018
ms.keywords: IClockVectorElement, IClockVectorElement interface [Windows Sync], IClockVectorElement interface [Windows Sync],described, winsync.iclockvectorelement, winsync/IClockVectorElement
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IClockVectorElement
 - winsync/IClockVectorElement
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - IClockVectorElement
---

# IClockVectorElement interface


## -description

Represents a clock vector element of a knowledge structure.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IClockVectorElement</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IClockVectorElement</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IClockVectorElement</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-iclockvectorelement-getreplicakey">GetReplicaKey</a>
</td>
<td align="left" width="63%">
Gets the replica key for the replica that is associated with this clock vector element.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-iclockvectorelement-gettickcount">GetTickCount</a>
</td>
<td align="left" width="63%">
Gets the tick count that defines the upper bound on the range of tick counts that are contained in this clock vector element.


</td>
</tr>
</table>

## -remarks

The clock vector elements of a clock vector represent the changes that are contained in a knowledge structure. A change that is made by a particular replica is defined to be contained in the knowledge when the tick count for the change occurs between zero and the tick count contained in the <b>IClockVectorElement</b> that tracks that replica.

## -see-also

<a href="/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>