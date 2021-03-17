---
UID: NF:vsprov.IVssFileShareSnapshotProvider.SetContext
title: IVssFileShareSnapshotProvider::SetContext (vsprov.h)
description: Sets the context for the subsequent shadow copy-related operations.
helpviewer_keywords: ["IVssFileShareSnapshotProvider interface [VSS]","SetContext method","IVssFileShareSnapshotProvider.SetContext","IVssFileShareSnapshotProvider::SetContext","SetContext","SetContext method [VSS]","SetContext method [VSS]","IVssFileShareSnapshotProvider interface","base.ivssfilesharesnapshotprovider_setcontext","vsprov/IVssFileShareSnapshotProvider::SetContext"]
old-location: base\ivssfilesharesnapshotprovider_setcontext.htm
tech.root: base
ms.assetid: 28e53076-4d8e-4f24-83b0-d0aaf7260802
ms.date: 12/05/2018
ms.keywords: IVssFileShareSnapshotProvider interface [VSS],SetContext method, IVssFileShareSnapshotProvider.SetContext, IVssFileShareSnapshotProvider::SetContext, SetContext, SetContext method [VSS], SetContext method [VSS],IVssFileShareSnapshotProvider interface, base.ivssfilesharesnapshotprovider_setcontext, vsprov/IVssFileShareSnapshotProvider::SetContext
req.header: vsprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - IVssFileShareSnapshotProvider::SetContext
 - vsprov/IVssFileShareSnapshotProvider::SetContext
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
 - IVssFileShareSnapshotProvider.SetContext
---

# IVssFileShareSnapshotProvider::SetContext


## -description

Sets the context for the subsequent shadow copy-related operations.

## -parameters

### -param lContext [in]

The context to be set. The context must be one of the supported values of <a href="/windows/desktop/api/vss/ne-vss-vss_snapshot_context">_VSS_SNAPSHOT_CONTEXT</a> or a supported combination of <a href="/windows/desktop/api/vss/ne-vss-vss_volume_snapshot_attributes">_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</a> and  <b>_VSS_SNAPSHOT_CONTEXT</b> values.

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
The context was set successfully.

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
<dt><b>VSS_E_BAD_STATE</b></dt>
</dl>
</td>
<td width="60%">
The context is frozen and cannot be changed.

</td>
</tr>
</table>

## -remarks

The default context for VSS shadow copies is VSS_CTX_BACKUP.

<b>Windows XP:  </b>The only supported context is the default context, VSS_CTX_BACKUP. Therefore, calling 
     <a href="/windows/desktop/api/vsprov/nf-vsprov-ivsssoftwaresnapshotprovider-setcontext">SetContext</a> under Windows XP returns
     E_NOTIMPL.

For more information about how the context that is set by 
    <a href="/windows/desktop/api/vsprov/nf-vsprov-ivsssoftwaresnapshotprovider-setcontext">SetContext</a> affects 
    how a shadow copy is created and managed, see 
    <a href="/windows/desktop/VSS/implementation-details-for-creating-shadow-copies">Implementation Details for 
    Creating Shadow Copies</a>.
   

For a complete discussion of the permitted shadow copy contexts, see 
    <a href="/windows/desktop/api/vss/ne-vss-vss_snapshot_context">_VSS_SNAPSHOT_CONTEXT</a> and 
    <a href="/windows/desktop/api/vss/ne-vss-vss_volume_snapshot_attributes">_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</a>.

## -see-also

<a href="/windows/desktop/api/vsprov/nn-vsprov-ivssfilesharesnapshotprovider">IVssFileShareSnapshotProvider</a>