---
UID: NF:winsync.IEnumSyncChangeUnits.Next
title: IEnumSyncChangeUnits::Next (winsync.h)
description: Returns the next change unit.
helpviewer_keywords: ["IEnumSyncChangeUnits interface [Windows Sync]","Next method","IEnumSyncChangeUnits.Next","IEnumSyncChangeUnits::Next","Next","Next method [Windows Sync]","Next method [Windows Sync]","IEnumSyncChangeUnits interface","winsync.ienumsyncchangeunits_next","winsync/IEnumSyncChangeUnits::Next"]
old-location: winsync\ienumsyncchangeunits_next.htm
tech.root: winsync
ms.assetid: e9d237fc-c651-4e94-83cc-8606fe4b2386
ms.date: 12/05/2018
ms.keywords: IEnumSyncChangeUnits interface [Windows Sync],Next method, IEnumSyncChangeUnits.Next, IEnumSyncChangeUnits::Next, Next, Next method [Windows Sync], Next method [Windows Sync],IEnumSyncChangeUnits interface, winsync.ienumsyncchangeunits_next, winsync/IEnumSyncChangeUnits::Next
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
 - IEnumSyncChangeUnits::Next
 - winsync/IEnumSyncChangeUnits::Next
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
 - IEnumSyncChangeUnits.Next
---

# IEnumSyncChangeUnits::Next


## -description

Returns the next change unit.

## -parameters

### -param cChanges [in]

The number of change units to fetch. The only valid value is 1.

### -param ppChangeUnit [out]

Returns the next change unit object.

### -param pcFetched [in, out]

Returns the number of change units that are fetched.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>

## -remarks

This method currently only supports retrieval of a single change unit. Therefore, <i>cChanges</i> must be 1. Otherwise, the call will fail.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ienumsyncchangeunits">IEnumSyncChangeUnits Interface</a>