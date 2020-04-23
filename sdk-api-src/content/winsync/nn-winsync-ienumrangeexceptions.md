---
UID: NN:winsync.IEnumRangeExceptions
title: IEnumRangeExceptions (winsync.h)
description: Enumerates range exceptions that are stored in a knowledge object.helpviewer_keywords: ["IEnumRangeExceptions","IEnumRangeExceptions interface [Windows Sync]","IEnumRangeExceptions interface [Windows Sync]","described","winsync.ienumrangeexceptions","winsync/IEnumRangeExceptions"]
old-location: winsync\ienumrangeexceptions.htm
tech.root: winsync
ms.assetid: 1b2724a3-2f5f-4f30-8cf5-e31f16d4cd14
ms.date: 12/05/2018
ms.keywords: IEnumRangeExceptions, IEnumRangeExceptions interface [Windows Sync], IEnumRangeExceptions interface [Windows Sync],described, winsync.ienumrangeexceptions, winsync/IEnumRangeExceptions
f1_keywords:
- winsync/IEnumRangeExceptions
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
- IEnumRangeExceptions
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumRangeExceptions interface


## -description


Enumerates range exceptions that are stored in a knowledge object.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumRangeExceptions</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumRangeExceptions</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumRangeExceptions</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-ienumrangeexceptions-clone">Clone</a>
</td>
<td align="left" width="63%">
Clones the enumerator and returns a new enumerator that is in the same state as the current one.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-ienumrangeexceptions-next">Next</a>
</td>
<td align="left" width="63%">
Returns the next elements in the range exception set, if they are available.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-ienumrangeexceptions-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator to the beginning of the range exception set.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-ienumrangeexceptions-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips the specified number of range exceptions.


</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
 

 

