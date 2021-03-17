---
UID: NF:winsync.ISyncChange.GetChangeUnits
title: ISyncChange::GetChangeUnits (winsync.h)
description: Gets an object that can enumerate change units that are contained in this change.
helpviewer_keywords: ["GetChangeUnits","GetChangeUnits method [Windows Sync]","GetChangeUnits method [Windows Sync]","ISyncChange interface","ISyncChange interface [Windows Sync]","GetChangeUnits method","ISyncChange.GetChangeUnits","ISyncChange::GetChangeUnits","winsync.isyncchange_getchangeunits","winsync/ISyncChange::GetChangeUnits"]
old-location: winsync\isyncchange_getchangeunits.htm
tech.root: winsync
ms.assetid: d3d0d805-ed29-4c88-925a-a16e130a3fe5
ms.date: 12/05/2018
ms.keywords: GetChangeUnits, GetChangeUnits method [Windows Sync], GetChangeUnits method [Windows Sync],ISyncChange interface, ISyncChange interface [Windows Sync],GetChangeUnits method, ISyncChange.GetChangeUnits, ISyncChange::GetChangeUnits, winsync.isyncchange_getchangeunits, winsync/ISyncChange::GetChangeUnits
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
 - ISyncChange::GetChangeUnits
 - winsync/ISyncChange::GetChangeUnits
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
 - ISyncChange.GetChangeUnits
---

# ISyncChange::GetChangeUnits


## -description

Gets an object that can enumerate change units that are contained in this change.

## -parameters

### -param ppEnum [out]

Returns a change unit enumerator. Returns <b>NULL</b> when this change does not contain change units.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_ITEM_HAS_NO_CHANGE_UNITS</b></dt>
</dl>
</td>
<td width="60%">
The change contains no change units.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchange">ISyncChange Interface</a>