---
UID: NF:winsync.ISyncChange.GetWorkEstimate
title: ISyncChange::GetWorkEstimate (winsync.h)
description: Gets the work estimate for this change.
helpviewer_keywords: ["GetWorkEstimate","GetWorkEstimate method [Windows Sync]","GetWorkEstimate method [Windows Sync]","ISyncChange interface","ISyncChange interface [Windows Sync]","GetWorkEstimate method","ISyncChange.GetWorkEstimate","ISyncChange::GetWorkEstimate","winsync.isyncchange_getworkestimate","winsync/ISyncChange::GetWorkEstimate"]
old-location: winsync\isyncchange_getworkestimate.htm
tech.root: winsync
ms.assetid: ba79bb88-bdeb-42be-88a9-1355fe048d10
ms.date: 12/05/2018
ms.keywords: GetWorkEstimate, GetWorkEstimate method [Windows Sync], GetWorkEstimate method [Windows Sync],ISyncChange interface, ISyncChange interface [Windows Sync],GetWorkEstimate method, ISyncChange.GetWorkEstimate, ISyncChange::GetWorkEstimate, winsync.isyncchange_getworkestimate, winsync/ISyncChange::GetWorkEstimate
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
 - ISyncChange::GetWorkEstimate
 - winsync/ISyncChange::GetWorkEstimate
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
 - ISyncChange.GetWorkEstimate
---

# ISyncChange::GetWorkEstimate


## -description

Gets the work estimate for this change.

## -parameters

### -param pdwWork [out]

The work estimate for this change. The default value is zero.

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

## -remarks

The work estimate is a part of the total work that is estimated for the batch or the session.

The work estimate is only meaningful when the <b>ISyncChange</b> object represents a change from the source provider.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchange">ISyncChange Interface</a>