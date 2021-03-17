---
UID: NF:vsbackup.IVssBackupComponents.PostRestore
title: IVssBackupComponents::PostRestore (vsbackup.h)
description: The PostRestore method will cause VSS to generate a PostRestore event, signaling writers that the current restore operation has finished.
helpviewer_keywords: ["IVssBackupComponents interface [VSS]","PostRestore method","IVssBackupComponents.PostRestore","IVssBackupComponents::PostRestore","PostRestore","PostRestore method [VSS]","PostRestore method [VSS]","IVssBackupComponents interface","_win32_ivssbackupcomponents_postrestore","base.ivssbackupcomponents_postrestore","vsbackup/IVssBackupComponents::PostRestore"]
old-location: base\ivssbackupcomponents_postrestore.htm
tech.root: base
ms.assetid: 01cf3931-59ef-4572-9f2e-aa210da0ac2d
ms.date: 12/05/2018
ms.keywords: IVssBackupComponents interface [VSS],PostRestore method, IVssBackupComponents.PostRestore, IVssBackupComponents::PostRestore, PostRestore, PostRestore method [VSS], PostRestore method [VSS],IVssBackupComponents interface, _win32_ivssbackupcomponents_postrestore, base.ivssbackupcomponents_postrestore, vsbackup/IVssBackupComponents::PostRestore
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - IVssBackupComponents::PostRestore
 - vsbackup/IVssBackupComponents::PostRestore
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
 - IVssBackupComponents.PostRestore
---

# IVssBackupComponents::PostRestore


## -description

The 
<b>PostRestore</b> method will cause VSS to generate a 
<b>PostRestore</b> event, signaling writers that the current restore operation has finished.

## -parameters

### -param ppAsync [out]

Doubly indirect pointer to an 
<a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a> object that contains status data for the signaled event.

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
Successfully returned the provider support information.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppAsync</i> does not point to a valid pointer; that is, it is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_BAD_STATE</b></dt>
</dl>
</td>
<td width="60%">
The backup components object is not initialized, this method has been called during a restore operation, or this method has not been called within the correct sequence.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_PROVIDER_VETO</b></dt>
</dl>
</td>
<td width="60%">
Expected provider error. The provider logged the error in the event log.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified volume was not found or was not available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error. The error code is logged in the error log file. For more information, see 
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
</table>

## -remarks

The caller is responsible for releasing the 
<a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a> interface.

## -see-also

<a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a>



<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prerestore">IVssBackupComponents::PreRestore</a>