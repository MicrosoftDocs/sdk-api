---
UID: NF:vsbackup.IVssBackupComponents.IsVolumeSupported
title: IVssBackupComponents::IsVolumeSupported (vsbackup.h)
description: The IsVolumeSupported method determines whether the specified provider supports shadow copies on the specified volume or remote file share.
helpviewer_keywords: ["IVssBackupComponents interface [VSS]","IsVolumeSupported method","IVssBackupComponents.IsVolumeSupported","IVssBackupComponents::IsVolumeSupported","IsVolumeSupported","IsVolumeSupported method [VSS]","IsVolumeSupported method [VSS]","IVssBackupComponents interface","_win32_ivssbackupcomponents_isvolumesupported","base.ivssbackupcomponents_isvolumesupported","vsbackup/IVssBackupComponents::IsVolumeSupported"]
old-location: base\ivssbackupcomponents_isvolumesupported.htm
tech.root: base
ms.assetid: 42e069cb-3d9a-4592-bbb8-0113f14ed28c
ms.date: 12/05/2018
ms.keywords: IVssBackupComponents interface [VSS],IsVolumeSupported method, IVssBackupComponents.IsVolumeSupported, IVssBackupComponents::IsVolumeSupported, IsVolumeSupported, IsVolumeSupported method [VSS], IsVolumeSupported method [VSS],IVssBackupComponents interface, _win32_ivssbackupcomponents_isvolumesupported, base.ivssbackupcomponents_isvolumesupported, vsbackup/IVssBackupComponents::IsVolumeSupported
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
 - IVssBackupComponents::IsVolumeSupported
 - vsbackup/IVssBackupComponents::IsVolumeSupported
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
 - IVssBackupComponents.IsVolumeSupported
---

# IVssBackupComponents::IsVolumeSupported


## -description

The 
<b>IsVolumeSupported</b> method determines whether the specified provider supports shadow copies on the specified volume or remote file share.

## -parameters

### -param ProviderId [in]

Provider identifier. If the value is GUID_NULL, 
<b>IsVolumeSupported</b> checks whether any provider supports the volume or remote file share.

### -param pwszVolumeName [in]

Volume name or UNC path of remote file share. The name or UNC path must be in one of the following formats and must include a trailing backslash (\\): 




<ul>
<li>The path of a mounted folder, for example, Y:\MountX\</li>
<li>A drive letter, for example, D:\</li>
<li>A volume GUID path of the form \\?&#92;<i>Volume</i>{<i>GUID</i>}\ (where <i>GUID</i> identifies the volume)</li>
<li>A UNC path that specifies a remote file share, for example, \\Clusterx\Share1\</li>
</ul>

### -param pbSupportedByThisProvider [out]

Address of a caller-allocated variable that receives <b>TRUE</b> if shadow copies are supported on the specified volume or remote file share, or <b>FALSE</b> otherwise.

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
<dt><b>VSS_E_NESTED_VOLUME_LIMIT</b></dt>
</dl>
</td>
<td width="60%">
The specified volume is nested too deeply to participate in the VSS operation.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This return code is not supported.

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
The backup components object is not initialized, this method has been called during a restore operation, or this method has not been called within the correct sequence.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified volume or remote file share was not found or was not available.

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

<b>Windows 7, Windows Server 2008 R2, Windows Vista, Windows Server 2008, Windows XP and Windows Server 2003:  </b>Remote file shares are not supported until Windows 8 and Windows Server 2012.

<b>IsVolumeSupported</b> will return <b>TRUE</b> if it is possible to create shadow copies on the given volume, even if the current configuration does not allow the creation of shadow copies on that volume at the present time.

For example, if the maximum number of shadow copies has been reached on a given volume (and therefore no more shadow copies can be created on that volume), the method will still indicate that the volume can be shadow copied.

<div class="alert"><b>Note</b>  For more information about the maximum number of shadow copies that can be created on a volume, see the entry for <b>MaxShadowCopies</b> in <a href="/windows/desktop/Backup/registry-keys-for-backup-and-restore">Registry Keys and Values for Backup and Restore</a>.</div>
<div> </div>
This method cannot be called for a virtual hard disk (VHD) that is nested inside another VHD.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>VHDs are not supported.

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset">IVssBackupComponents::AddToSnapshotSet</a>