---
UID: NF:winsync.ISyncChangeUnit.GetChangeUnitId
title: ISyncChangeUnit::GetChangeUnitId (winsync.h)
description: Retrieves the ID for this change unit.
helpviewer_keywords: ["GetChangeUnitId","GetChangeUnitId method [Windows Sync]","GetChangeUnitId method [Windows Sync]","ISyncChangeUnit interface","ISyncChangeUnit interface [Windows Sync]","GetChangeUnitId method","ISyncChangeUnit.GetChangeUnitId","ISyncChangeUnit::GetChangeUnitId","winsync.isyncchangeunit_getchangeunitid","winsync/ISyncChangeUnit::GetChangeUnitId"]
old-location: winsync\isyncchangeunit_getchangeunitid.htm
tech.root: winsync
ms.assetid: 956f2d51-3b14-4bbd-8a29-6d63aa3c344f
ms.date: 12/05/2018
ms.keywords: GetChangeUnitId, GetChangeUnitId method [Windows Sync], GetChangeUnitId method [Windows Sync],ISyncChangeUnit interface, ISyncChangeUnit interface [Windows Sync],GetChangeUnitId method, ISyncChangeUnit.GetChangeUnitId, ISyncChangeUnit::GetChangeUnitId, winsync.isyncchangeunit_getchangeunitid, winsync/ISyncChangeUnit::GetChangeUnitId
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
 - ISyncChangeUnit::GetChangeUnitId
 - winsync/ISyncChangeUnit::GetChangeUnitId
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
 - ISyncChangeUnit.GetChangeUnitId
---

# ISyncChangeUnit::GetChangeUnitId


## -description

Retrieves the ID for this change unit.

## -parameters

### -param pbChangeUnitId [in, out]

Returns the ID of the change unit.

### -param pcbIdSize [in, out]

Specifies the number of bytes in <i>pbChangeUnitId</i>. Returns the number of bytes required to retrieve the ID if <i>pbChangeUnitId</i> is too small, or returns the number of bytes written.

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
<dt><b>HRESULT_FROM_WIN32(ERROR_MORE_DATA)</b></dt>
</dl>
</td>
<td width="60%">
<i>pbChangeUnitId</i> is too small. In this case, the required number of bytes is returned in <i>pcbIdSize</i>.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangeunit">ISyncChangeUnit Interface</a>