---
UID: NF:vswriter.IVssCreateWriterMetadata.AddFilesToFileGroup
title: IVssCreateWriterMetadata::AddFilesToFileGroup (vswriter.h)
description: The AddFilesToFileGroup method adds a file set (a specified file or files) to a specified file group component.
helpviewer_keywords: ["AddFilesToFileGroup","AddFilesToFileGroup method [VSS]","AddFilesToFileGroup method [VSS]","IVssCreateWriterMetadata interface","IVssCreateWriterMetadata interface [VSS]","AddFilesToFileGroup method","IVssCreateWriterMetadata.AddFilesToFileGroup","IVssCreateWriterMetadata::AddFilesToFileGroup","_win32_ivsscreatewritermetadata_addfilestofilegroup","base.ivsscreatewritermetadata_addfilestofilegroup","vswriter/IVssCreateWriterMetadata::AddFilesToFileGroup"]
old-location: base\ivsscreatewritermetadata_addfilestofilegroup.htm
tech.root: base
ms.assetid: 5d5a0155-467c-4c42-876e-a1b245cf6f8e
ms.date: 12/05/2018
ms.keywords: AddFilesToFileGroup, AddFilesToFileGroup method [VSS], AddFilesToFileGroup method [VSS],IVssCreateWriterMetadata interface, IVssCreateWriterMetadata interface [VSS],AddFilesToFileGroup method, IVssCreateWriterMetadata.AddFilesToFileGroup, IVssCreateWriterMetadata::AddFilesToFileGroup, _win32_ivsscreatewritermetadata_addfilestofilegroup, base.ivsscreatewritermetadata_addfilestofilegroup, vswriter/IVssCreateWriterMetadata::AddFilesToFileGroup
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
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
 - IVssCreateWriterMetadata::AddFilesToFileGroup
 - vswriter/IVssCreateWriterMetadata::AddFilesToFileGroup
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
 - IVssCreateWriterMetadata.AddFilesToFileGroup
---

# IVssCreateWriterMetadata::AddFilesToFileGroup


## -description

The 
<b>AddFilesToFileGroup</b> method adds a file set (a specified file or files) to a specified file group component.

## -parameters

### -param wszLogicalPath [in]

Pointer to a <b>null</b>-terminated wide character string containing the logical path (which may be <b>NULL</b>) of the component to which to add the files. For more information, see <a href="/windows/desktop/VSS/logical-pathing-of-components">Logical Pathing of Components</a>.

### -param wszGroupName [in]

Pointer to a <b>null</b>-terminated wide character string containing the name of the file group component. The type of this component must be VSS_CT_FILEGROUP; otherwise, the method will return an error.

### -param wszPath [in]

Pointer to a <b>null</b>-terminated wide character string containing the default root directory of the files to be added. 




The directory can be a local directory on the VSS machine, or it can be a file share directory on a remote file server.

UNC paths are supported.

The path can contain environment variables (for example, %SystemRoot%) but cannot contain wildcard characters.

There is no requirement that the path end with a backslash ("\"). It is up to applications that retrieve this information to check.

### -param wszFilespec [in]

Pointer to a <b>null</b>-terminated wide character string containing the file specification of the files to be included. 




A file specification cannot contain directory specifications (for example, no backslashes) but can contain the ? and * wildcard characters.

### -param bRecursive [in]

A Boolean value specifying whether the path specified by the <i>wszPath</i> parameter identifies only a single directory or if it indicates a hierarchy of directories to be traversed recursively. This parameter should be set to <b>true</b> if the path is treated as a hierarchy of directories to be recursed through, or <b>false</b> otherwise. 




For information on traversing over mounted folders, see 
<a href="/windows/desktop/VSS/working-with-reparse-and-mount-points">Working with Mounted Folders and Reparse Points</a>.

### -param wszAlternateLocation [in]

Pointer to a <b>null</b>-terminated wide character string containing the alternate path, which actually contains the files to be backed up with this component.

 The directory can be a local directory on the VSS machine, or it can be a file share directory on a remote file server.

UNC paths are supported.

Specifying an alternate path is optional; if no alternate path is needed, <i>wszAlternatePath</i> should be <b>NULL</b>.

An alternate path should not be confused with an alternate location mapping.

### -param dwBackupTypeMask [in]

A bitmask of 
<a href="/windows/desktop/api/vss/ne-vss-vss_file_spec_backup_type">VSS_FILE_SPEC_BACKUP_TYPE</a> enumeration values to indicate if a writer should evaluate the file for participation in a certain type of backup operations. 




The default value for this argument is (VSS_FSBT_ALL_BACKUP_REQUIRED | VSS_FSBT_ALL_SNAPSHOT_REQUIRED).

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
The operation was successful.

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
One of the parameter values is not valid, or the caller attempted to add file-group files to a non-file-group component.

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
<dt><b>VSS_E_INVALID_XML_DOCUMENT</b></dt>
<dt>0x80042311L</dt>
</dl>
</td>
<td width="60%">
The XML document is not valid. Check the event log for details. For more information, see 
<a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_NOT_SUPPORTED</b></dt>
<dt>0x8004232FL</dt>
</dl>
</td>
<td width="60%">
For express writers, the value of <i>wszAlternatePath</i> must be <b>NULL</b>, and the <i>dwBackupTypeMask</i> bitmask cannot include <b>VSS_FSBT_DIFFERENTIAL_BACKUP_REQUIRED</b>, <b>VSS_FSBT_INCREMENTAL_BACKUP_REQUIRED</b>, or <b>VSS_FSBT_LOG_BACKUP_REQUIRED</b>.

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
The specified component does not exist.

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

<b>Windows 7, Windows Server 2008 R2, Windows Vista, Windows Server 2008, Windows XP and Windows Server 2003:  </b>Remote file shares are not supported until Windows 8 and Windows Server 2012. Writers support only local resources—sets of files whose absolute path starts with a valid local volume specification and cannot be a mapped network drive. Therefore, path inputs (<i>wszPath</i> and <i>wszAlternatePath</i>) to 
<b>AddFilesToFileGroup</b> (after the resolution of any environment variables) must be in this format.

A writer can call this method multiple times to add several sets of files to its file group component. However, you should make sure that the file specifications do not overlap, because a particular file can be specified only once.

The locations from which files are backed up and to which they are restored depends on the values for the root directory defined by <i>wszPath</i> and the alternate path defined by <i>wszAlternatePath</i>.

Note the following when using path information provided by 
<b>AddFilesToFileGroup</b>:

<ul>
<li>Restore operations should (if possible) restore files added to a component by 
<b>AddFilesToFileGroup</b> under the default root directory defined by <i>wszPath</i>.</li>
<li>If an alternate path is not specified (if <i>wszAlternatePath</i> is <b>NULL</b>), the files added to the component will be backed up from the default root directory and restored to the default root directory indicated by <i>wszPath</i>.</li>
<li>If an alternate path is specified (if <i>wszAlternatePath</i> is non-<b>NULL</b>), files added to the component are backed up from the alternate path specified by <i>wszAlternatePath</i>. However, requesters will still use <i>wszPath</i> as the default restoration location.</li>
<li>If the alternate path is defined (<i>wszAlternatePath</i> is non-<b>NULL</b>) and there are files matching the file specification (<i>wszFilespec</i>) in both the alternate path and the default root directory (<i>wszPath</i>), then a backup operation should back up files located under the alternate path, not files located under the default root directory.</li>
<li>Files should be restored to the directory indicated by <i>wszPath</i> unless an alternate location mapping was set by 
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping">IVssCreateWriterMetadata::AddAlternateLocationMapping</a> and the restore method or restore target requires it.</li>
</ul>
For more information on backup and restore file locations under VSS, see 
<a href="/windows/desktop/VSS/non-default-backup-and-restore-locations">Non-Default Backup And Restore Locations</a>.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscreatewritermetadata">IVssCreateWriterMetadata</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping">IVssCreateWriterMetadata::AddAlternateLocationMapping</a>