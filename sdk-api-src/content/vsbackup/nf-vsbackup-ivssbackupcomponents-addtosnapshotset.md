---
UID: NF:vsbackup.IVssBackupComponents.AddToSnapshotSet
title: IVssBackupComponents::AddToSnapshotSet (vsbackup.h)
description: The AddToSnapshotSet method adds an original volume or original remote file share to the shadow copy set.
helpviewer_keywords: ["AddToSnapshotSet","AddToSnapshotSet method [VSS]","AddToSnapshotSet method [VSS]","IVssBackupComponents interface","IVssBackupComponents interface [VSS]","AddToSnapshotSet method","IVssBackupComponents.AddToSnapshotSet","IVssBackupComponents::AddToSnapshotSet","_win32_ivssbackupcomponents_addtosnapshotset","base.ivssbackupcomponents_addtosnapshotset","vsbackup/IVssBackupComponents::AddToSnapshotSet"]
old-location: base\ivssbackupcomponents_addtosnapshotset.htm
tech.root: base
ms.assetid: 6c20e386-7cd8-45d9-92d6-96d0a458db50
ms.date: 12/05/2018
ms.keywords: AddToSnapshotSet, AddToSnapshotSet method [VSS], AddToSnapshotSet method [VSS],IVssBackupComponents interface, IVssBackupComponents interface [VSS],AddToSnapshotSet method, IVssBackupComponents.AddToSnapshotSet, IVssBackupComponents::AddToSnapshotSet, _win32_ivssbackupcomponents_addtosnapshotset, base.ivssbackupcomponents_addtosnapshotset, vsbackup/IVssBackupComponents::AddToSnapshotSet
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
 - IVssBackupComponents::AddToSnapshotSet
 - vsbackup/IVssBackupComponents::AddToSnapshotSet
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
 - IVssBackupComponents.AddToSnapshotSet
---

# IVssBackupComponents::AddToSnapshotSet


## -description

The <b>AddToSnapshotSet</b> method adds 
    an original volume or original remote file share to the shadow copy set.

## -parameters

### -param pwszVolumeName [in]

Null-terminated wide character string containing the name of the volume or the UNC path of the remote file share to be shadow copied. The name or UNC path must be in one of the following formats and must include a trailing backslash (\\): 
      

<ul>
<li>The path of a mounted folder, for example, Y:\MountX\</li>
<li>A drive letter, for example, D:\</li>
<li>A volume GUID path of the form \\?&#92;<i>Volume</i>{<i>GUID</i>}\ (where <i>GUID</i> identifies the volume)</li>
<li>A UNC path that specifies a remote file share, for example, \\Clusterx\Share1\</li>
</ul>

### -param ProviderId [in]

The provider to be used. GUID_NULL can be used, in which case the default provider will be used.

### -param pidSnapshot [out]

Returned identifier of the added shadow copy.

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
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
Successfully added the volume or remote file share to the shadow copy set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
<dt>0x80070005L</dt>
</dl>
</td>
<td width="60%">
Caller does not have sufficient backup privileges or is not an administrator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
<dt>0x80070057L</dt>
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
<dt>0x8007000EL</dt>
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
<dt>0x80042301L</dt>
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
<dt><b>VSS_E_MAXIMUM_NUMBER_OF_VOLUMES_REACHED</b></dt>
<dt>0x80042312L</dt>
</dl>
</td>
<td width="60%">
The maximum number of volumes or remote file shares have been added to the shadow copy set. The specified volume or remote file share was not added to 
        the shadow copy set.
       

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_MAXIMUM_NUMBER_OF_SNAPSHOTS_REACHED</b></dt>
<dt>0x80042317L</dt>
</dl>
</td>
<td width="60%">
The volume or remote file share has been added to the maximum number of shadow copy sets. The specified volume or remote file share was not added to 
        the shadow copy set.
       

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_NESTED_VOLUME_LIMIT</b></dt>
<dt>0x8004232CL</dt>
</dl>
</td>
<td width="60%">
The specified volume is nested too deeply to participate in the VSS operation. Possible reasons for this error include the following:

<ul>
<li>Trying to create a shadow copy of a volume that resides on a VHD that is contained in another VHD.</li>
<li>Trying to create a shadow copy of a VHD volume when the volume that contains the VHD is also in the same shadow copy set.</li>
</ul>
<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This return code is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
<dt>0x80042308L</dt>
</dl>
</td>
<td width="60%">
<i>pwszVolumeName</i> does not correspond to an existing volume  or remote file share.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_PROVIDER_NOT_REGISTERED</b></dt>
<dt>0x80042304L</dt>
</dl>
</td>
<td width="60%">
<i>ProviderId</i> does not correspond to a registered provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_PROVIDER_VETO</b></dt>
<dt>0x80042306L</dt>
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
<dt><b>VSS_E_SNAPSHOT_SET_IN_PROGRESS</b></dt>
<dt>0x80042316L</dt>
</dl>
</td>
<td width="60%">
Another shadow copy creation is already in progress.  Occurs when adding a CSV volume to a snapshot set from multiple nodes at the same time, or while adding a scale out share to the snapshot set from multiple SMB client nodes at the same time.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_VOLUME_NOT_SUPPORTED</b></dt>
<dt>0x8004230CL</dt>
</dl>
</td>
<td width="60%">
The value of the <i>ProviderId</i> parameter is GUID_NULL and no VSS provider indicates 
        that it supports the specified volume or remote file share.
       

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_VOLUME_NOT_SUPPORTED_BY_PROVIDER</b></dt>
<dt>0x8004230EL</dt>
</dl>
</td>
<td width="60%">
The volume or remote file share is not supported by the specified provider.

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
<dt>0x8004230FL</dt>
</dl>
</td>
<td width="60%">
The provider returned an unexpected error code. This error code is only returned via the 
        <a href="/windows/desktop/api/vss/nf-vss-ivssasync-querystatus">QueryStatus</a> method on the 
        <a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a> interface returned in the 
        <i>ppAsync</i> parameter.
       

</td>
</tr>
</table>

## -remarks

<b>Windows 7, Windows Server 2008 R2, Windows Vista, Windows Server 2008, Windows XP and Windows Server 2003:  </b>Remote file shares are not supported until Windows 8 and Windows Server 2012.

If <i>pwszVolumeName</i> is a UNC share path, the server name portion must be in hostname or fully qualified domain name format. UNC share names with IP addresses must be normalized by calling the <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponentsex4-getrootandlogicalprefixpaths">IVssBackupComponentsEx4::GetRootAndLogicalPrefixPaths</a> method before they are passed to <b>AddToSnapshotSet</b>.

The maximum number of shadow copied volumes in a single shadow copy set is 64.

If <i>ProviderId</i> is GUID_NULL, the default provider is selected according to the 
    following algorithm:
   

<ol>
<li>If any hardware provider supports the given volume or remote file share, that provider is selected.</li>
<li>If there is no hardware provider available, if any software provider supports the given volume, it 
      is selected.
     </li>
<li>If there is no hardware provider or software provider available, the system provider is selected. 
      (There is only one preinstalled system provider, which must support all nonremovable local volumes.)
     </li>
</ol>
This method cannot be called for a virtual hard disk (VHD) that is nested inside another VHD.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>VHDs are not supported.

The shadow copy identifier that is returned in the <i>pidSnapshot</i> parameter is stored in the Backup Components Document. However, there is no method for querying this information, and the caller may need to store it so that it can be used during restore.

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponentsex4-getrootandlogicalprefixpaths">IVssBackupComponentsEx4::GetRootAndLogicalPrefixPaths</a>



<a href="/windows/desktop/api/vss/ne-vss-vss_volume_snapshot_attributes">_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</a>