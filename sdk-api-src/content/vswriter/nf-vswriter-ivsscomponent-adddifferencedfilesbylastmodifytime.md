---
UID: NF:vswriter.IVssComponent.AddDifferencedFilesByLastModifyTime
title: IVssComponent::AddDifferencedFilesByLastModifyTime (vswriter.h)
description: Used by a writer to indicate that a file set (a specified file or files) should be evaluated against a last modification time stamp for inclusion in a time stamped incremental or differential backup using entire files.
helpviewer_keywords: ["AddDifferencedFilesByLastModifyTime","AddDifferencedFilesByLastModifyTime method [VSS]","AddDifferencedFilesByLastModifyTime method [VSS]","IVssComponent interface","IVssComponent interface [VSS]","AddDifferencedFilesByLastModifyTime method","IVssComponent.AddDifferencedFilesByLastModifyTime","IVssComponent::AddDifferencedFilesByLastModifyTime","_win32_ivsscomponent_adddifferencedfilesbylastmodifytime","base.ivsscomponent_adddifferencedfilesbylastmodifytime","vswriter/IVssComponent::AddDifferencedFilesByLastModifyTime"]
old-location: base\ivsscomponent_adddifferencedfilesbylastmodifytime.htm
tech.root: base
ms.assetid: 33372d10-c947-45de-9ea2-03ba6378179d
ms.date: 12/05/2018
ms.keywords: AddDifferencedFilesByLastModifyTime, AddDifferencedFilesByLastModifyTime method [VSS], AddDifferencedFilesByLastModifyTime method [VSS],IVssComponent interface, IVssComponent interface [VSS],AddDifferencedFilesByLastModifyTime method, IVssComponent.AddDifferencedFilesByLastModifyTime, IVssComponent::AddDifferencedFilesByLastModifyTime, _win32_ivsscomponent_adddifferencedfilesbylastmodifytime, base.ivsscomponent_adddifferencedfilesbylastmodifytime, vswriter/IVssComponent::AddDifferencedFilesByLastModifyTime
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
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
 - IVssComponent::AddDifferencedFilesByLastModifyTime
 - vswriter/IVssComponent::AddDifferencedFilesByLastModifyTime
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
 - IVssComponent.AddDifferencedFilesByLastModifyTime
---

# IVssComponent::AddDifferencedFilesByLastModifyTime


## -description

The 
    <b>AddDifferencedFilesByLastModifyTime</b> 
    method is used by a writer to indicate that a file set (a specified file or files) should be evaluated against a 
    last modification time stamp for inclusion in a time stamped incremental or differential backup using entire 
    files, not partial files.

This method can be called by a writer only during a backup operation.

## -parameters

### -param wszPath [in]

Null-terminated wide character string containing the name of the directory or directory hierarchy 
      containing the files to be mapped.
      

The path can contain environment variables (for example, %SystemRoot%) but cannot contain wildcard 
       characters.

There is no requirement that the path end with a backslash ("\"). It is up to applications that 
       retrieve this information to check.

### -param wszFilespec [in]

Null-terminated wide character string containing the file specification of the files to be mapped.
      

A file specification cannot contain directory specifications (for example, no backslashes) but can contain 
       the ? and * wildcard characters.

### -param bRecursive [in]

A Boolean value specifying whether the path specified by the <i>wszPath</i> parameter identifies 
      only a single directory or if it indicates a hierarchy of directories to be traversed recursively. This parameter should be set to <b>true</b> if the path is treated as a hierarchy of directories to be traversed recursively, or  <b>false</b> if not.
      

For information on traversing mounted folders, see 
       <a href="/windows/desktop/VSS/working-with-reparse-and-mount-points">Working with Mounted Folders and Reparse Points</a>.

### -param ftLastModifyTime [in]

The writer specification of the time of last modification for the difference files, expressed as a 
      <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure.
      

The last-modify time is always given in Greenwich Mean Time.

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
Successfully added differenced files.

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
This method was not called by a writer or, if called by a writer, it either was not called during a 
        backup operation or was called while handling a 
        <a href="/windows/desktop/VSS/vssgloss-b">BackupComplete</a> or 
        <a href="/windows/desktop/VSS/vssgloss-b">BackupShutdown</a> event.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_INVALID_XML_DOCUMENT</b></dt>
</dl>
</td>
<td width="60%">
The XML document is not valid. Check the event log for details. For more 
        information, see 
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
</table>

## -remarks

A writer calls this method to specify that certain files in a component should be backed up only if they have been modified since a certain time. For more information, see <a href="/windows/desktop/VSS/writer-role-in-backing-up-complex-stores">Backup By Last Modify Time</a>.

This method can be called only by writers supporting the last modified schema 
    (<b>VSS_BS_LAST_MODIFY</b>), and only during backup operations. Writers using this method do 
    not have to support the time-stamp schema (<b>VSS_BS_TIMESTAMPED</b>).

Files added by 
    <b>AddDifferencedFilesByLastModifyTime</b> 
    should not also be added by 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-addpartialfile">IVssComponent::AddPartialFile</a>.

If the backup type (<a href="/windows/desktop/api/vss/ne-vss-vss_backup_type">VSS_BACKUP_TYPE</a>) is incremental 
    (<b>VSS_BT_INCREMENTAL</b>), writers using 
    <b>AddDifferencedFilesByLastModifyTime</b> 
    must support the incremental schema (<b>VSS_BS_INCREMENTAL</b>). If the backup type is 
    differential, the writer must support the <b>VSS_BS_DIFFERENTIAL</b> schema.

The 
    <b>AddDifferencedFilesByLastModifyTime</b> 
    method should be called prior to the actual start of a backup operation, typically while handling the 
    <a href="/windows/desktop/VSS/vssgloss-p">PostSnapshot</a> event (see 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostsnapshot">CVssWriter::OnPostSnapshot</a>).

If the time-stamp value set by 
    <b>AddDifferencedFilesByLastModifyTime</b> 
    is nonzero, a requester must respect this value regardless of its own records and file system information when 
    determining if the differenced file should be included in a differential or incremental backup.

If the time stamp set by 
    <b>AddDifferencedFilesByLastModifyTime</b> 
    (<i>ftLastModifyTime</i>) is zero, the requester can use file system information and its own 
    records to determine whether the differenced files should be included in a differential or incremental backup.

Requesters retrieve the number of differenced files managed by a component by calling 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getdifferencedfile">IVssComponent::GetDifferencedFile</a>.

Differenced file sets can be either of the following:

<ul>
<li>A member of the current component or (if the component defines a component set) its subcomponents</li>
<li>New files not previously included in the component or subcomponents. The 
      <b>AddDifferencedFilesByLastModifyTime</b> 
      method allows writers to indicate that files created since the original backup should be included in the 
      component to support incremental or differential backups.</li>
</ul>
When referring to files that are already part of the component, the combination of path, file specification, 
    and recursion flag (<i>wszPath</i>, <i>wszFileSpec</i>, and 
    <i>bRecursive</i>, respectively) provided to 
    <b>AddDifferencedFilesByLastModifyTime</b> 
    to be mapped must match that of one of the file sets added to a component by 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup">IVssCreateWriterMetadata::AddFilesToFileGroup</a>, 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles">IVssCreateWriterMetadata::AddDatabaseFiles</a>, or 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles">IVssCreateWriterMetadata::AddDatabaseLogFiles</a>.

When adding new files to the component, 
    <b>AddDifferencedFilesByLastModifyTime</b>, 
    the writer should not add files managed by another component or writer.

There is no method in the 
    <a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a> interface that allows for changing or adding 
    an alternate location mappings for new files added by 
    <b>AddDifferencedFilesByLastModifyTime</b>. 
    If an alternate location mapping corresponds to the new file, then that alternate location will be used.

## -see-also

<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostsnapshot">CVssWriter::OnPostSnapshot</a>



<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getdifferencedfile">IVssComponent::GetDifferencedFile</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getdifferencedfilescount">IVssComponent::GetDifferencedFilesCount</a>



<a href="/windows/desktop/VSS/incremental-and-differential-backups">Incremental and Differential Backups</a>



<a href="/windows/desktop/api/vss/ne-vss-vss_backup_schema">VSS_BACKUP_SCHEMA</a>



<a href="/windows/desktop/api/vss/ne-vss-vss_backup_type">VSS_BACKUP_TYPE</a>



<a href="/windows/desktop/api/vss/ne-vss-vss_file_spec_backup_type">VSS_FILE_SPEC_BACKUP_TYPE</a>