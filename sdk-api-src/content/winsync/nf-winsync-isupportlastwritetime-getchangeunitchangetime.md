---
UID: NF:winsync.ISupportLastWriteTime.GetChangeUnitChangeTime
title: ISupportLastWriteTime::GetChangeUnitChangeTime (winsync.h)
description: Gets the date and time when the specified change unit was last changed.
helpviewer_keywords: ["GetChangeUnitChangeTime","GetChangeUnitChangeTime method [Windows Sync]","GetChangeUnitChangeTime method [Windows Sync]","ISupportLastWriteTime interface","ISupportLastWriteTime interface [Windows Sync]","GetChangeUnitChangeTime method","ISupportLastWriteTime.GetChangeUnitChangeTime","ISupportLastWriteTime::GetChangeUnitChangeTime","winsync.isupportlastwritetime_getchangeunitchangetime","winsync/ISupportLastWriteTime::GetChangeUnitChangeTime"]
old-location: winsync\isupportlastwritetime_getchangeunitchangetime.htm
tech.root: winsync
ms.assetid: f289d5a5-c991-4223-b59a-68b31ecffb8c
ms.date: 12/05/2018
ms.keywords: GetChangeUnitChangeTime, GetChangeUnitChangeTime method [Windows Sync], GetChangeUnitChangeTime method [Windows Sync],ISupportLastWriteTime interface, ISupportLastWriteTime interface [Windows Sync],GetChangeUnitChangeTime method, ISupportLastWriteTime.GetChangeUnitChangeTime, ISupportLastWriteTime::GetChangeUnitChangeTime, winsync.isupportlastwritetime_getchangeunitchangetime, winsync/ISupportLastWriteTime::GetChangeUnitChangeTime
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - ISupportLastWriteTime::GetChangeUnitChangeTime
 - winsync/ISupportLastWriteTime::GetChangeUnitChangeTime
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
 - ISupportLastWriteTime.GetChangeUnitChangeTime
---

# ISupportLastWriteTime::GetChangeUnitChangeTime


## -description

Gets the date and time when the specified change unit was last changed.

## -parameters

### -param pbItemId [in]

The ID of the item that contains the change unit to look up.

### -param pbChangeUnitId [in]

The ID of the change unit to look up.

### -param pullTimestamp [out]

The date and time when the specified change unit was last changed.

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
<dt><b>Provider-determined error codes</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isupportlastwritetime">ISupportLastWriteTime Interface</a>