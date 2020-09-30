---
UID: NF:winsync.IFeedClockVector.IsNoConflictsSpecified
title: IFeedClockVector::IsNoConflictsSpecified (winsync.h)
description: Gets a value that indicates whether conflicts are preserved for the FeedSync item.
helpviewer_keywords: ["IFeedClockVector interface [Windows Sync]","IsNoConflictsSpecified method","IFeedClockVector.IsNoConflictsSpecified","IFeedClockVector::IsNoConflictsSpecified","IsNoConflictsSpecified","IsNoConflictsSpecified method [Windows Sync]","IsNoConflictsSpecified method [Windows Sync]","IFeedClockVector interface","winsync.ifeedclockvector_isnoconflictsspecified","winsync/IFeedClockVector::IsNoConflictsSpecified"]
old-location: winsync\ifeedclockvector_isnoconflictsspecified.htm
tech.root: winsync
ms.assetid: d43d193b-d0c4-4b01-be90-a322fcc8b672
ms.date: 12/05/2018
ms.keywords: IFeedClockVector interface [Windows Sync],IsNoConflictsSpecified method, IFeedClockVector.IsNoConflictsSpecified, IFeedClockVector::IsNoConflictsSpecified, IsNoConflictsSpecified, IsNoConflictsSpecified method [Windows Sync], IsNoConflictsSpecified method [Windows Sync],IFeedClockVector interface, winsync.ifeedclockvector_isnoconflictsspecified, winsync/IFeedClockVector::IsNoConflictsSpecified
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
 - IFeedClockVector::IsNoConflictsSpecified
 - winsync/IFeedClockVector::IsNoConflictsSpecified
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
 - IFeedClockVector.IsNoConflictsSpecified
---

# IFeedClockVector::IsNoConflictsSpecified


## -description

Gets a value that indicates whether conflicts are preserved for the FeedSync item.

## -parameters

### -param pfIsNoConflictsSpecified [out]

TRUE if conflicts are not preserved for the item; otherwise, <b>FALSE</b>. This value corresponds to the <b>noconflicts</b> attribute of the FeedSync item.

## -returns

The possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ifeedclockvector">IFeedClockVector Interface</a>