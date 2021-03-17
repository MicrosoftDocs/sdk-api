---
UID: NF:vsbackup.IVssBackupComponents.AddNewTarget
title: IVssBackupComponents::AddNewTarget (vsbackup.h)
description: The AddNewTarget method is used by a requester during a restore operation to indicate that the backup application plans to restore files to a new location.
helpviewer_keywords: ["AddNewTarget","AddNewTarget method [VSS]","AddNewTarget method [VSS]","IVssBackupComponents interface","IVssBackupComponents interface [VSS]","AddNewTarget method","IVssBackupComponents.AddNewTarget","IVssBackupComponents::AddNewTarget","_win32_ivssbackupcomponents_addnewtarget","base.ivssbackupcomponents_addnewtarget","vsbackup/IVssBackupComponents::AddNewTarget"]
old-location: base\ivssbackupcomponents_addnewtarget.htm
tech.root: base
ms.assetid: 9a4e2638-f6e7-4264-997d-41880f23c981
ms.date: 12/05/2018
ms.keywords: AddNewTarget, AddNewTarget method [VSS], AddNewTarget method [VSS],IVssBackupComponents interface, IVssBackupComponents interface [VSS],AddNewTarget method, IVssBackupComponents.AddNewTarget, IVssBackupComponents::AddNewTarget, _win32_ivssbackupcomponents_addnewtarget, base.ivssbackupcomponents_addnewtarget, vsbackup/IVssBackupComponents::AddNewTarget
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
 - IVssBackupComponents::AddNewTarget
 - vsbackup/IVssBackupComponents::AddNewTarget
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
 - IVssBackupComponents.AddNewTarget
---

# IVssBackupComponents::AddNewTarget


## -description

The 
<b>AddNewTarget</b> method is used by a requester during a restore operation to indicate that the backup application plans to restore files to a new location.

## -parameters

### -param writerId [in]

Globally unique identifier (GUID) of the writer class containing the files that are to receive a new target.

### -param ct [in]

Identifies the type of the component. Refer to the documentation for 
<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_component_type">VSS_COMPONENT_TYPE</a> for possible return values.

### -param wszLogicalPath [in]

<b>Null</b>-terminated wide character string containing the logical path of the component containing the files that are to receive a new restore target. For more information, see <a href="/windows/desktop/VSS/logical-pathing-of-components">Logical Pathing of Components</a>. 




The value of the string containing the logical path used here should be the same as was used when the component was added to the backup set using 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addcomponent">IVssBackupComponents::AddComponent</a>.

The logical path can be <b>NULL</b>.

There are no restrictions on the characters that can appear in a non-<b>NULL</b> logical path.

### -param wszComponentName [in]

<b>Null</b>-terminated wide character string containing the name of the component containing the files that are to receive a new restore target. 




The string should not be <b>NULL</b> and should contain the same component name as was used when the component was added to the backup set using 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addcomponent">IVssBackupComponents::AddComponent</a>.

There are no restrictions on the characters that can appear in a non-<b>NULL</b> logical path.

### -param wszPath [in]

<b>Null</b>-terminated wide character string containing the name of the directory or directory hierarchy containing the files to receive a new restore target. 




The directory can be a local directory on the VSS machine, or it can be a file share directory on a remote file server.

The path can contain environment variables (for example, %SystemRoot%) but cannot contain wildcard characters. UNC paths are supported.

There is no requirement that the path end with a backslash ("\"). It is up to applications that retrieve this information to check.

### -param wszFileName [in]

<b>Null</b>-terminated wide character string containing the file specification of the files to receive a new restore target. 




A file specification cannot contain directory specifications (for example, no backslashes) but can contain the ? and * wildcard characters.

### -param bRecursive [in]

Boolean indicating whether only the files in the directory defined by <i>wszPath</i> and matching the file specification provided by <i>wszFileName</i> are to receive a new restore target, or if all files in the hierarchy defined by <i>wszPath</i> and matching the file specification provided by <i>wszFileName</i> are to receive a new restore target. 




For information on traversing mounted folders, see 
<a href="/windows/desktop/VSS/working-with-reparse-and-mount-points">Working with Mounted Folders and Reparse Points</a>.

### -param wszAlternatePath [in]

<b>Null</b>-terminated wide character string containing the fully qualified path of the new restore target directory. 

The directory can be a local directory on the VSS machine, or it can be a file share directory on a remote file server.

UNC paths are supported.

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
Successfully added the new restore target.

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
The backup components object is not initialized, or this method has been called during a restore operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_INVALID_XML_DOCUMENT</b></dt>
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
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The component does not exist or the path and file specification do not match a component and file specification in the component.

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

The component name specified as an argument to 
<b>AddNewTarget</b> (<i>wszComponentName</i>) must match a component that has already been added to the Backup Components Document.

Therefore, <i>wszComponentName</i> can be the name of any component explicitly included in the Backup Components Document.

Adding a new target for file in a subcomponent must be done using the name of the component that defines the component set containing the subcomponent.

When specifying a file or files to have their restore target changed, a requester must ensure that the combination of path, file specification, and recursion flag (<i>wszPath</i>, <i>wszFileSpec</i>, and  <i>bRecursive</i>, respectively) provided to 
<b>AddNewTarget</b> must match that of one of the file sets added to a component using 
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup">IVssCreateWriterMetadata::AddFilesToFileGroup</a>, 
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles">IVssCreateWriterMetadata::AddDatabaseFiles</a>, or 
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles">IVssCreateWriterMetadata::AddDatabaseLogFiles</a>.

When a requester calls <b>AddNewTarget</b>, it must do so before calling <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prerestore">IVssBackupComponents::PreRestore</a>. For more information, see <a href="/windows/desktop/VSS/overview-of-preparing-for-restore">Overview of Preparing for Restore</a>.

Path and file descriptor information can be obtained from the Writer Metadata Document by using the 
<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswmfiledesc">IVssWMFiledesc</a> object returned by 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivsswmcomponent-getfile">IVssWMComponent::GetFile</a>, 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivsswmcomponent-getdatabasefile">IVssWMComponent::GetDatabaseFile</a>, or 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile">IVssWMComponent::GetDatabaseLogFile</a>. The 
<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivsswmcomponent">IVssWMComponent</a> object is obtained from Writer Metadata Document by the 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent">IVssExamineWriterMetadata::GetComponent</a> method.

Writers can determine if files have been restored to new locations by using the 
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getnewtargetcount">IVssComponent::GetNewTargetCount</a> and 
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getnewtarget">IVssComponent::GetNewTarget</a> methods.

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addcomponent">IVssBackupComponents::AddComponent</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getnewtarget">IVssComponent::GetNewTarget</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getnewtargetcount">IVssComponent::GetNewTargetCount</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles">IVssCreateWriterMetadata::AddDatabaseFiles</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles">IVssCreateWriterMetadata::AddDatabaseLogFiles</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup">IVssCreateWriterMetadata::AddFilesToFileGroup</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent">IVssExamineWriterMetadata::GetComponent</a>



<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivsswmcomponent">IVssWMComponent</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivsswmcomponent-getdatabasefile">IVssWMComponent::GetDatabaseFile</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile">IVssWMComponent::GetDatabaseLogFile</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivsswmcomponent-getfile">IVssWMComponent::GetFile</a>



<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswmfiledesc">IVssWMFiledesc</a>



<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_component_type">VSS_COMPONENT_TYPE</a>