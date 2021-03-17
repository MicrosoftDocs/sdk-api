---
UID: NF:winsync.ISyncChange.SetWorkEstimate
title: ISyncChange::SetWorkEstimate (winsync.h)
description: Sets the work estimate for this change.
helpviewer_keywords: ["ISyncChange interface [Windows Sync]","SetWorkEstimate method","ISyncChange.SetWorkEstimate","ISyncChange::SetWorkEstimate","SetWorkEstimate","SetWorkEstimate method [Windows Sync]","SetWorkEstimate method [Windows Sync]","ISyncChange interface","winsync.isyncchange_setworkestimate","winsync/ISyncChange::SetWorkEstimate"]
old-location: winsync\isyncchange_setworkestimate.htm
tech.root: winsync
ms.assetid: 2f26cc10-ff0c-448e-a174-edca0b0b2e10
ms.date: 12/05/2018
ms.keywords: ISyncChange interface [Windows Sync],SetWorkEstimate method, ISyncChange.SetWorkEstimate, ISyncChange::SetWorkEstimate, SetWorkEstimate, SetWorkEstimate method [Windows Sync], SetWorkEstimate method [Windows Sync],ISyncChange interface, winsync.isyncchange_setworkestimate, winsync/ISyncChange::SetWorkEstimate
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
 - ISyncChange::SetWorkEstimate
 - winsync/ISyncChange::SetWorkEstimate
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
 - ISyncChange.SetWorkEstimate
---

# ISyncChange::SetWorkEstimate


## -description

Sets the work estimate for this change.

## -parameters

### -param dwWork [in]

The work estimate for this change.

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
</table>

## -remarks

The work estimate is a part of the total work that is estimated for the batch or the session.

The work estimate is only meaningful when the <b>ISyncChange</b> object represents a change from the source provider.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchange">ISyncChange Interface</a>