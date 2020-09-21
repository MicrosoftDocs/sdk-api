---
UID: NF:vsbackup.IVssBackupComponentsEx2.UnexposeSnapshot
title: IVssBackupComponentsEx2::UnexposeSnapshot (vsbackup.h)
description: Unexposes a shadow copy either by deleting the file share or by removing the drive letter or mounted folder.
helpviewer_keywords: ["IVssBackupComponentsEx2 interface","UnexposeSnapshot method","IVssBackupComponentsEx2.UnexposeSnapshot","IVssBackupComponentsEx2::UnexposeSnapshot","UnexposeSnapshot","UnexposeSnapshot method","UnexposeSnapshot method","IVssBackupComponentsEx2 interface","base.ivssbackupcomponentsex2_unexposesnapshot","vsbackup/IVssBackupComponentsEx2::UnexposeSnapshot"]
old-location: base\ivssbackupcomponentsex2_unexposesnapshot.htm
tech.root: base
ms.assetid: b6946b65-b142-41b9-88c0-a1b11caba08e
ms.date: 12/05/2018
ms.keywords: IVssBackupComponentsEx2 interface,UnexposeSnapshot method, IVssBackupComponentsEx2.UnexposeSnapshot, IVssBackupComponentsEx2::UnexposeSnapshot, UnexposeSnapshot, UnexposeSnapshot method, UnexposeSnapshot method,IVssBackupComponentsEx2 interface, base.ivssbackupcomponentsex2_unexposesnapshot, vsbackup/IVssBackupComponentsEx2::UnexposeSnapshot
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IVssBackupComponentsEx2::UnexposeSnapshot
 - vsbackup/IVssBackupComponentsEx2::UnexposeSnapshot
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
 - IVssBackupComponentsEx2.UnexposeSnapshot
---

# IVssBackupComponentsEx2::UnexposeSnapshot


## -description

Unexposes a shadow copy either by deleting the file share or by removing the drive letter or mounted folder.

## -parameters

### -param snapshotId [in]

The shadow copy identifier. The value of this identifier should be the same as the value that was used when the shadow copy was exposed.

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
The shadow copy was successfully unexposed.

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
The backup components object is not initialized, this method has been called during a restore operation, or 
        this method has not been called within the correct sequence.
       

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified shadow copy does not exist or is not exposed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_PROVIDER_VETO</b></dt>
</dl>
</td>
<td width="60%">
An
        expected provider error has occurred. The error code is logged in the event log. For more information, see 
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

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
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_UNEXPECTED_PROVIDER_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An unexpected provider error has occurred. The error code is logged in the error log. For more information, see 
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot">IVssBackupComponents::ExposeSnapshot</a>



<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponentsex2">IVssBackupComponentsEx2</a>