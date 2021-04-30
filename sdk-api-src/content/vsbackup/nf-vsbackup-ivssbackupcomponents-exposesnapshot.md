---
UID: NF:vsbackup.IVssBackupComponents.ExposeSnapshot
title: IVssBackupComponents::ExposeSnapshot (vsbackup.h)
description: The ExposeSnapshot method exposes a shadow copy as a drive letter, mounted folder, or file share.
helpviewer_keywords: ["ExposeSnapshot","ExposeSnapshot method [VSS]","ExposeSnapshot method [VSS]","IVssBackupComponents interface","IVssBackupComponents interface [VSS]","ExposeSnapshot method","IVssBackupComponents.ExposeSnapshot","IVssBackupComponents::ExposeSnapshot","_win32_ivssbackupcomponents_exposesnapshot","base.ivssbackupcomponents_exposesnapshot","vsbackup/IVssBackupComponents::ExposeSnapshot"]
old-location: base\ivssbackupcomponents_exposesnapshot.htm
tech.root: base
ms.assetid: 5a0abafa-d770-4529-90e4-0c597729d525
ms.date: 12/05/2018
ms.keywords: ExposeSnapshot, ExposeSnapshot method [VSS], ExposeSnapshot method [VSS],IVssBackupComponents interface, IVssBackupComponents interface [VSS],ExposeSnapshot method, IVssBackupComponents.ExposeSnapshot, IVssBackupComponents::ExposeSnapshot, _win32_ivssbackupcomponents_exposesnapshot, base.ivssbackupcomponents_exposesnapshot, vsbackup/IVssBackupComponents::ExposeSnapshot
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
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
 - IVssBackupComponents::ExposeSnapshot
 - vsbackup/IVssBackupComponents::ExposeSnapshot
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
 - IVssBackupComponents.ExposeSnapshot
---

# IVssBackupComponents::ExposeSnapshot


## -description

The <b>ExposeSnapshot</b> method exposes a 
    shadow copy as a drive letter, mounted folder, or file share.

## -parameters

### -param SnapshotId [in]

Shadow copy identifier.

### -param wszPathFromRoot [in]

The path to the portion of the volume made available when exposing a shadow copy as a file share. The value of 
      this parameter must be <b>NULL</b> when exposing a shadow copy locally; that is, exposing it as a drive letter or mounted folder. 
      

The path cannot contain environment variables (for example, %MyEnv%) or wildcard characters.

There is no requirement that the path end with a backslash ("\"). It is up to applications that
       retrieve this information to check.

### -param lAttributes [in]

Attributes of the exposed shadow copy indicating whether it is exposed locally or remotely. The value must be 
      either the <b>VSS_VOLSNAP_ATTR_EXPOSED_LOCALLY</b> or the 
      <b>VSS_VOLSNAP_ATTR_EXPOSED_REMOTELY</b> value of 
      <a href="/windows/desktop/api/vss/ne-vss-vss_volume_snapshot_attributes">_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</a>.

### -param wszExpose [in]

When a shadow copy is exposed as a file share, the value of this parameter is the share name. If a shadow copy 
      is exposed by mounting it as a device, the parameter value is a drive letter followed by a colon—for
      example, "X:" or a mounted folder path (for example, "Y:\MountX"). If the value of this parameter is <b>NULL</b>, then VSS
      determines the share name or drive letter if the <i>lAttributes</i> parameter is 
      <b>VSS_VOLSNAP_ATTR_EXPOSED_REMOTELY</b>.

### -param pwszExposed [out]

The exposed name of the shadow copy. This is either a share name, a drive letter followed by a colon, 
      or a mounted folder. The value is <b>NULL</b> if 
      <b>ExposeSnapshot</b> failed.
     VSS allocates the memory for this string.

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
The shadow copies were successfully exposed.

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
The specified shadow copy does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_PROVIDER_VETO</b></dt>
</dl>
</td>
<td width="60%">
Expected provider error. The provider logged the error in the event log. For more information, see 
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
Unexpected provider error. The error code is logged in the error log. For more information, see 
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.
       

</td>
</tr>
</table>

## -remarks

The caller is responsible for freeing the string that  the <i>pwszExposed</i> parameter points to by calling the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

When exposing a persistent shadow copy, it remains exposed through subsequent boots.

When exposing a shadow copy of a volume, the shadow copy may be treated either as a mountable device or as a file 
    system available for file sharing.
   

When it is exposed as a device—as with other mountable devices—the shadow copy of a volume is exposed 
    at its mount point (drive letter or mounted folder) starting with its root.
   

When exposed as a file share, subsets (indicated by <i>wszPathFromRoot</i>) of the volume can 
    be shared.
   

For more information on how to expose shadow copies, see 
    <a href="/windows/desktop/VSS/exposing-and-surfacing-shadow-copied-volumes">Exposing and Surfacing Shadow Copied
    Volumes</a>.

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-importsnapshots">IVssBackupComponents::ImportSnapshots</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponentsex2-unexposesnapshot">IVssBackupComponentsEx2::UnexposeSnapshot</a>



<a href="/windows/desktop/VSS/volume-shadow-copy-api-data-types">VSS_PWSZ</a>



<a href="/windows/desktop/api/vss/ne-vss-vss_volume_snapshot_attributes">_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</a>