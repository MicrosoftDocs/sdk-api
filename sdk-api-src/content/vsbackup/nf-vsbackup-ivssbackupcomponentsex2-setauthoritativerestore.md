---
UID: NF:vsbackup.IVssBackupComponentsEx2.SetAuthoritativeRestore
title: IVssBackupComponentsEx2::SetAuthoritativeRestore (vsbackup.h)
description: Marks the restore of a component as authoritative for a replicated data store.
helpviewer_keywords: ["IVssBackupComponentsEx2 interface","SetAuthoritativeRestore method","IVssBackupComponentsEx2.SetAuthoritativeRestore","IVssBackupComponentsEx2::SetAuthoritativeRestore","SetAuthoritativeRestore","SetAuthoritativeRestore method","SetAuthoritativeRestore method","IVssBackupComponentsEx2 interface","base.ivssbackupcomponentsex2_setauthoritativerestore","vsbackup/IVssBackupComponentsEx2::SetAuthoritativeRestore"]
old-location: base\ivssbackupcomponentsex2_setauthoritativerestore.htm
tech.root: base
ms.assetid: 3725a282-2df8-4a0a-a1bf-a73c2b259cbf
ms.date: 12/05/2018
ms.keywords: IVssBackupComponentsEx2 interface,SetAuthoritativeRestore method, IVssBackupComponentsEx2.SetAuthoritativeRestore, IVssBackupComponentsEx2::SetAuthoritativeRestore, SetAuthoritativeRestore, SetAuthoritativeRestore method, SetAuthoritativeRestore method,IVssBackupComponentsEx2 interface, base.ivssbackupcomponentsex2_setauthoritativerestore, vsbackup/IVssBackupComponentsEx2::SetAuthoritativeRestore
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
 - IVssBackupComponentsEx2::SetAuthoritativeRestore
 - vsbackup/IVssBackupComponentsEx2::SetAuthoritativeRestore
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
 - IVssBackupComponentsEx2.SetAuthoritativeRestore
---

# IVssBackupComponentsEx2::SetAuthoritativeRestore


## -description

Marks the restore of a component as authoritative for a replicated data store.

## -parameters

### -param writerId [in]

The globally unique identifier (GUID) of the writer class.

### -param ct [in]

The type of the component. See the <a href="/windows/desktop/api/vswriter/ne-vswriter-vss_component_type">VSS_COMPONENT_TYPE</a> 
      enumeration for the possible values.

### -param wszLogicalPath [in]

A <b>null</b>-terminated wide character string containing the logical path of the component. 
      For more information, see <a href="/windows/desktop/VSS/logical-pathing-of-components">Logical Pathing of Components</a>.

The value of the string containing the logical path used here should be the same as the string that was used when the 
       component was added.

The logical path can be <b>NULL</b>.

There are no restrictions on the characters that can appear in a non-<b>NULL</b> logical path.

### -param wszComponentName [in]

A <b>null</b>-terminated wide character string containing the name of the component. 
     

The string cannot be <b>NULL</b> and should contain the same component name as the string that was used when the component was added 
      to the backup set using 
      the <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addcomponent">IVssBackupComponents::AddComponent</a> method.

### -param bAuth [in]

Set this variable to <b>true</b> to indicate that the restore of the component is authoritative, or <b>false</b> otherwise.

The default value is <b>false</b>.

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
The restore of the component was successfully set to authoritative or nonauthoritative.

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
This method was not called during a restore operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified component was not found.

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

The <b>SetAuthoritativeRestore</b> method can only be called during a restore operation.

A writer indicates that it supports authoritative restore by setting the <b>VSS_BS_AUTHORITATIVE_RESTORE</b> flag in its backup schema mask.

For more 
      information, see <a href="/windows/desktop/VSS/setting-vss-restore-options">Setting VSS Restore 
      Options</a>.

## -see-also

<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions">IVssBackupComponents::SetRestoreOptions</a>



<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponentsex2">IVssBackupComponentsEx2</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponentex-getauthoritativerestore">IVssComponentEx::GetAuthoritativeRestore</a>



<a href="/windows/desktop/api/vss/ne-vss-vss_backup_schema">VSS_BACKUP_SCHEMA</a>