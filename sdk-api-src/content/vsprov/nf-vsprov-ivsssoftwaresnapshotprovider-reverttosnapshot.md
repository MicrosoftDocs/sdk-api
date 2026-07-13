---
UID: NF:vsprov.IVssSoftwareSnapshotProvider.RevertToSnapshot
title: IVssSoftwareSnapshotProvider::RevertToSnapshot (vsprov.h)
description: Reverts a volume to a previous shadow copy. (IVssSoftwareSnapshotProvider.RevertToSnapshot)
helpviewer_keywords: ["IVssSoftwareSnapshotProvider interface","RevertToSnapshot method","IVssSoftwareSnapshotProvider.RevertToSnapshot","IVssSoftwareSnapshotProvider::RevertToSnapshot","RevertToSnapshot","RevertToSnapshot method","RevertToSnapshot method","IVssSoftwareSnapshotProvider interface","base.ivsssoftwaresnapshotprovider_reverttosnapshot","vsprov/IVssSoftwareSnapshotProvider::RevertToSnapshot"]
old-location: base\ivsssoftwaresnapshotprovider_reverttosnapshot.htm
tech.root: base
ms.assetid: 55c55bbc-b40e-4659-bee6-2448e6b6a4df
ms.date: 12/05/2018
ms.keywords: IVssSoftwareSnapshotProvider interface,RevertToSnapshot method, IVssSoftwareSnapshotProvider.RevertToSnapshot, IVssSoftwareSnapshotProvider::RevertToSnapshot, RevertToSnapshot, RevertToSnapshot method, RevertToSnapshot method,IVssSoftwareSnapshotProvider interface, base.ivsssoftwaresnapshotprovider_reverttosnapshot, vsprov/IVssSoftwareSnapshotProvider::RevertToSnapshot
req.header: vsprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: VssApi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssSoftwareSnapshotProvider::RevertToSnapshot
 - vsprov/IVssSoftwareSnapshotProvider::RevertToSnapshot
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssSoftwareSnapshotProvider.RevertToSnapshot
---

# IVssSoftwareSnapshotProvider::RevertToSnapshot


## -description

Reverts a volume to a previous shadow copy. Only shadow copies created with persistent contexts (VSS_CTX_APP_ROLLBACK, VSS_CTX_CLIENT_ACCESSIBLE, VSS_CTX_CLIENT_ACCESSIBLE_WRITERS, or VSS_CTX_NAS_ROLLBACK) are supported.

## -parameters

### -param SnapshotId [in]

Shadow copy identifier of the shadow copy to revert.

## -returns

The following are the valid return codes for this method.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The revert operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient backup privileges or is not an administrator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameter values is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The caller is out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_REVERT_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
The volume already has a revert operation in process.

</td>
</tr>
</table>

## -remarks

This operation cannot be canceled, or undone once completed. If the computer is rebooted during the revert operation, the revert process will continue when the system is restarted.

## -see-also

<a href="/windows/desktop/api/vsprov/nn-vsprov-ivsssoftwaresnapshotprovider">IVssSoftwareSnapshotProvider</a>
