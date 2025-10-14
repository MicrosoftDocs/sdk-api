---
UID: NF:vsbackup.IVssBackupComponents.RevertToSnapshot
title: IVssBackupComponents::RevertToSnapshot (vsbackup.h)
description: Reverts a volume to a previous shadow copy. (IVssBackupComponents.RevertToSnapshot)
helpviewer_keywords: ["IVssBackupComponents interface [VSS]","RevertToSnapshot method","IVssBackupComponents.RevertToSnapshot","IVssBackupComponents::RevertToSnapshot","RevertToSnapshot","RevertToSnapshot method [VSS]","RevertToSnapshot method [VSS]","IVssBackupComponents interface","_win32_ivssbackupcomponents_reverttosnapshot","base.ivssbackupcomponents_reverttosnapshot","vsbackup/IVssBackupComponents::RevertToSnapshot"]
old-location: base\ivssbackupcomponents_reverttosnapshot.htm
tech.root: base
ms.assetid: 9976195e-3448-4b0e-82b2-1ae061c75b17
ms.date: 12/05/2018
ms.keywords: IVssBackupComponents interface [VSS],RevertToSnapshot method, IVssBackupComponents.RevertToSnapshot, IVssBackupComponents::RevertToSnapshot, RevertToSnapshot, RevertToSnapshot method [VSS], RevertToSnapshot method [VSS],IVssBackupComponents interface, _win32_ivssbackupcomponents_reverttosnapshot, base.ivssbackupcomponents_reverttosnapshot, vsbackup/IVssBackupComponents::RevertToSnapshot
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
 - IVssBackupComponents::RevertToSnapshot
 - vsbackup/IVssBackupComponents::RevertToSnapshot
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
 - IVssBackupComponents.RevertToSnapshot
---

# IVssBackupComponents::RevertToSnapshot


## -description

The <b>RevertToSnapshot</b> method 
   reverts a volume to a previous shadow copy. Only shadow copies created with persistent contexts 
   (<b>VSS_CTX_APP_ROLLBACK</b>, <b>VSS_CTX_CLIENT_ACCESSIBLE</b>, 
   <b>VSS_CTX_CLIENT_ACCESSIBLE_WRITERS</b>, or 
   <b>VSS_CTX_NAS_ROLLBACK</b>) are supported.
<div class="alert"><b>Note</b>  This method is only supported on Windows Server operating systems.</div><div> </div>

## -parameters

### -param SnapshotId [in]

VSS_ID of the shadow copy to revert.

### -param bForceDismount [in]

If this parameter is 
      <b>TRUE</b>, the volume will be dismounted and reverted even if the volume is in use.

## -returns

This method can return one of these values.

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
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The calling process has insufficient privileges.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
There is an internal error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters passed is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The provider for the volume does not support revert operations.

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
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The <i>SnapshotId</i> parameter is not a valid shadow copy.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_PROVIDER_NOT_REGISTERED</b></dt>
</dl>
</td>
<td width="60%">
The provider was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_REVERT_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
The volume already has a revert in process.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_UNSUPPORTED_CONTEXT</b></dt>
</dl>
</td>
<td width="60%">
Revert is only supported for persistent shadow copies.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_VOLUME_IN_USE</b></dt>
</dl>
</td>
<td width="60%">
The <i>bForceDismount</i> parameter was <b>FALSE</b>, and the 
        volume could not be locked.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_VOLUME_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Revert is not supported on this volume.

</td>
</tr>
</table>

## -remarks

This operation cannot be canceled, or undone once completed. If the computer is rebooted during the revert 
     operation, the revert process will continue when the system is restarted.

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-queryrevertstatus">IVssBackupComponents::QueryRevertStatus</a>
