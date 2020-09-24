---
UID: NF:winsync.ISyncChangeUnit.GetChangeUnitVersion
title: ISyncChangeUnit::GetChangeUnitVersion (winsync.h)
description: Gets the version for the change unit change.
helpviewer_keywords: ["GetChangeUnitVersion","GetChangeUnitVersion method [Windows Sync]","GetChangeUnitVersion method [Windows Sync]","ISyncChangeUnit interface","ISyncChangeUnit interface [Windows Sync]","GetChangeUnitVersion method","ISyncChangeUnit.GetChangeUnitVersion","ISyncChangeUnit::GetChangeUnitVersion","winsync.isyncchangeunit_getchangeunitversion","winsync/ISyncChangeUnit::GetChangeUnitVersion"]
old-location: winsync\isyncchangeunit_getchangeunitversion.htm
tech.root: winsync
ms.assetid: b40ec132-0459-4ddf-9156-bce2a1dfbc4d
ms.date: 12/05/2018
ms.keywords: GetChangeUnitVersion, GetChangeUnitVersion method [Windows Sync], GetChangeUnitVersion method [Windows Sync],ISyncChangeUnit interface, ISyncChangeUnit interface [Windows Sync],GetChangeUnitVersion method, ISyncChangeUnit.GetChangeUnitVersion, ISyncChangeUnit::GetChangeUnitVersion, winsync.isyncchangeunit_getchangeunitversion, winsync/ISyncChangeUnit::GetChangeUnitVersion
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
 - ISyncChangeUnit::GetChangeUnitVersion
 - winsync/ISyncChangeUnit::GetChangeUnitVersion
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
 - ISyncChangeUnit.GetChangeUnitVersion
---

# ISyncChangeUnit::GetChangeUnitVersion


## -description

Gets the version for the change unit change.

## -parameters

### -param pbCurrentReplicaId [in]

The ID of the replica that originated the change to retrieve.

### -param pVersion [out]

Returns the version of the change.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pbCurrentReplicaId</i> is not the correct replica ID.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangeunit">ISyncChangeUnit Interface</a>



<a href="/windows/desktop/api/winsync/ns-winsync-sync_version">SYNC_VERSION Structure</a>