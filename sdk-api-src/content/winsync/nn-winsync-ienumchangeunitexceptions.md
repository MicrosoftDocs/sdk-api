---
UID: NN:winsync.IEnumChangeUnitExceptions
title: IEnumChangeUnitExceptions (winsync.h)
description: Enumerates change unit exceptions that are stored in a knowledge object.
helpviewer_keywords: ["IEnumChangeUnitExceptions","IEnumChangeUnitExceptions interface [Windows Sync]","IEnumChangeUnitExceptions interface [Windows Sync]","described","winsync.ienumchangeunitexceptions","winsync/IEnumChangeUnitExceptions"]
old-location: winsync\ienumchangeunitexceptions.htm
tech.root: winsync
ms.assetid: 40b2977e-f3ae-4ad2-89ed-aacf32b1171e
ms.date: 12/05/2018
ms.keywords: IEnumChangeUnitExceptions, IEnumChangeUnitExceptions interface [Windows Sync], IEnumChangeUnitExceptions interface [Windows Sync],described, winsync.ienumchangeunitexceptions, winsync/IEnumChangeUnitExceptions
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
 - IEnumChangeUnitExceptions
 - winsync/IEnumChangeUnitExceptions
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
 - IEnumChangeUnitExceptions
---

# IEnumChangeUnitExceptions interface


## -description

Enumerates change unit exceptions that are stored in a knowledge object.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumChangeUnitExceptions</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumChangeUnitExceptions</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumChangeUnitExceptions</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-ienumchangeunitexceptions-clone">Clone</a>
</td>
<td align="left" width="63%">
Clones the enumerator and returns a new enumerator that is in the same state as the current one.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-ienumchangeunitexceptions-next">Next</a>
</td>
<td align="left" width="63%">
Returns the next elements in the change unit exception set, if they are available.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-ienumchangeunitexceptions-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator to the beginning of the change unit exception set.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-ienumchangeunitexceptions-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips the specified number of change unit exceptions.


</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>