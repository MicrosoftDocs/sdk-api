---
UID: NN:winsync.IEnumClockVector
title: IEnumClockVector (winsync.h)
author: windows-sdk-content
description: Enumerates the clock vector elements that are stored in a clock vector.
old-location: winsync\ienumclockvector.htm
tech.root: winsync
ms.assetid: cf191502-dc51-44a7-a82f-a0e38537574f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumClockVector, IEnumClockVector interface [Windows Sync], IEnumClockVector interface [Windows Sync],described, winsync.ienumclockvector, winsync/IEnumClockVector
ms.topic: interface
f1_keywords: 
 - "winsync/IEnumClockVector"
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
 - IEnumClockVector
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumClockVector interface


## -description


Enumerates the clock vector elements that are stored in a clock vector.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumClockVector</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumClockVector</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumClockVector</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-ienumclockvector-clone">Clone</a>
</td>
<td align="left" width="63%">
Clones the enumerator and returns a new enumerator that is in the same state as the current one.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-ienumclockvector-next">Next</a>
</td>
<td align="left" width="63%">
Returns the next elements in the clock vector, if they are available.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-ienumclockvector-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator to the beginning of the clock vector.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-ienumclockvector-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips the specified number of clock vector elements.


</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
 

 

