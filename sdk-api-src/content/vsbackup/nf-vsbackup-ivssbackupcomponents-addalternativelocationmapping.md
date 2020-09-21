---
UID: NF:vsbackup.IVssBackupComponents.AddAlternativeLocationMapping
title: IVssBackupComponents::AddAlternativeLocationMapping (vsbackup.h)
description: The AddAlternativeLocationMapping method is used by a requester to indicate that an alternate location mapping was used to restore all the members of a file set in a given component.
helpviewer_keywords: ["AddAlternativeLocationMapping","AddAlternativeLocationMapping method [VSS]","AddAlternativeLocationMapping method [VSS]","IVssBackupComponents interface","IVssBackupComponents interface [VSS]","AddAlternativeLocationMapping method","IVssBackupComponents.AddAlternativeLocationMapping","IVssBackupComponents::AddAlternativeLocationMapping","_win32_ivssbackupcomponents_addalternativelocationmapping","base.ivssbackupcomponents_addalternativelocationmapping","vsbackup/IVssBackupComponents::AddAlternativeLocationMapping"]
old-location: base\ivssbackupcomponents_addalternativelocationmapping.htm
tech.root: base
ms.assetid: 349ec124-f3f5-4142-8600-8d9f508c9bb2
ms.date: 12/05/2018
ms.keywords: AddAlternativeLocationMapping, AddAlternativeLocationMapping method [VSS], AddAlternativeLocationMapping method [VSS],IVssBackupComponents interface, IVssBackupComponents interface [VSS],AddAlternativeLocationMapping method, IVssBackupComponents.AddAlternativeLocationMapping, IVssBackupComponents::AddAlternativeLocationMapping, _win32_ivssbackupcomponents_addalternativelocationmapping, base.ivssbackupcomponents_addalternativelocationmapping, vsbackup/IVssBackupComponents::AddAlternativeLocationMapping
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
 - IVssBackupComponents::AddAlternativeLocationMapping
 - vsbackup/IVssBackupComponents::AddAlternativeLocationMapping
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
 - IVssBackupComponents.AddAlternativeLocationMapping
---

# IVssBackupComponents::AddAlternativeLocationMapping


## -description

The 
<b>AddAlternativeLocationMapping</b> method is used by a requester to indicate that an alternate location mapping was used to restore all the members of a file set in a given component.

## -parameters

### -param writerId [in]

Globally unique identifier (GUID) of the writer class that exported the component.

### -param componentType [in]

Type of the component. The possible values of this parameter are defined by the 
<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_component_type">VSS_COMPONENT_TYPE</a> enumeration.

### -param wszLogicalPath [in]

<b>Null</b>-terminated wide character string containing the logical path to the component. 


For more information, see <a href="/windows/desktop/VSS/logical-pathing-of-components">Logical Pathing of Components</a>.

The logical path can be <b>NULL</b>.

There are no restrictions on the characters that can appear in a non-<b>NULL</b> logical path.

### -param wszComponentName [in]

<b>Null</b>-terminated wide character string containing the component name. 




There are no restrictions on the characters that can appear in a non-<b>NULL</b> logical path.

### -param wszPath [in]

<b>Null</b>-terminated wide character string containing the path to the directory that originally contained the file to be relocated. This path can be local to the VSS machine, or it can be a file share directory on a remote file server. 




The path can contain environment variables (for example, %SystemRoot%) but cannot contain wildcard characters. UNC paths are supported.

There is no requirement that the path end with a backslash ("\"). It is up to applications that retrieve this information to check.

### -param wszFilespec [in]

<b>Null</b>-terminated wide character string containing the original file specification. 




A file specification cannot contain directory specifications (for example, no backslashes) but can contain the ? and * wildcard characters.

### -param bRecursive [in]

A Boolean value that indicates whether the path specified by the <i>wszPath</i> parameter identifies only a single directory or if it indicates a hierarchy of directories to be traversed recursively. This parameter should be set to <b>true</b> if the path is treated as a hierarchy of directories to be traversed recursively, or <b>false</b> if not. 




For information on traversing mounted folders, see 
<a href="/windows/desktop/VSS/working-with-reparse-and-mount-points">Working with Mounted Folders and Reparse Points</a>.

### -param wszDestination [in]

<b>Null</b>-terminated wide character string containing the name of the directory where the file will be relocated. This path can be local to the VSS machine, or it can be a file share directory on a remote file server. UNC paths are supported.

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
Successfully added the alternate location mapping.

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
The backup components object is not initialized, this method has been called during a restore operation, or this method has not been called within the correct sequence.

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

<b>Windows 7, Windows Server 2008 R2, Windows Vista, Windows Server 2008, Windows XP and Windows Server 2003:  </b>Remote file shares are not supported until Windows 8 and Windows Server 2012.

The <i>writerId</i>, <i>componentType</i>, <i>wszLogicalPath</i>, and <i>wszComponentName</i> parameters identify a particular component, and the <i>wszPath</i>, <i>wszFilespec</i>, and <i>bRecursive</i> parameters identify the file set belonging to that component.

The combination of path, file specification, and recursion flag (<i>wszPath</i>, <i>wszFilespec</i>, and <i>bRecursive</i>, respectively) provided to 
<b>AddAlternativeLocationMapping</b> to be mapped must match that of one of the file sets added to a component using either 
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup">IVssCreateWriterMetadata::AddFilesToFileGroup</a>, 
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles">IVssCreateWriterMetadata::AddDatabaseFiles</a>, or 
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles">IVssCreateWriterMetadata::AddDatabaseLogFiles</a>.

Because 
<b>AddAlternativeLocationMapping</b> is used to notify a writer that an alternate location was used to restore all the files in a component, it should not be called for any component or files in a component that have not had an alternate location mapping specified.

The value of <i>wszPath</i> will have been mapped to <i>wszDestination</i> on restore; however, file names and subdirectories under the original path retain their same names.

A typical usage of 
<b>AddAlternativeLocationMapping</b> during restore might be the following:

<ol>
<li>Retrieve stored Writer Metadata Documents from the backup media and load that information with 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-loadfromxml">IVssExamineWriterMetadata::LoadFromXML</a>.</li>
<li>Call 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping">IVssExamineWriterMetadata::GetAlternateLocationMapping</a> to get an 
<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswmfiledesc">IVssWMFiledesc</a> interface with the mapping information and use 
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsswmfiledesc-getalternatelocation">IVssWMFiledesc::GetAlternateLocation</a> to get the alternate location.</li>
<li>Examine filedesc information to heuristically determine which component this alternate location mapping should be applied to.</li>
<li>Call 
<b>IVssBackupComponents::AddAlternativeLocationMapping</b> to communicate where files were restored.</li>
</ol>
A file should always be restored to its alternate location mapping if either of the following is true:

<ul>
<li>The restore method (set at backup time) is VSS_RME_RESTORE_TO_ALTERNATE_LOCATION.</li>
<li>Its restore target was set (at restore time) to VSS_RT_ALTERNATE.</li>
</ul>
In either case, if no valid alternate location mapping is defined this constitutes a writer error.

A file may be restored to an alternate location mapping if either of the following is true:

<ul>
<li>The restore method is VSS_RME_RESTORE_IF_NOT_THERE and a version of the file is already present on disk.</li>
<li>The restore method is VSS_RME_RESTORE_IF_CAN_REPLACE and a version of the file is present on disk and cannot be replaced.</li>
</ul>
Again, if no valid alternate location mapping is defined this constitutes a writer error.

An alternate location mapping is used only during a restore operation and should not be confused with an alternate path, which is used only during a backup operation.

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsswmfiledesc-getalternatelocation">IVssWMFiledesc::GetAlternateLocation</a>



<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_component_type">VSS_COMPONENT_TYPE</a>