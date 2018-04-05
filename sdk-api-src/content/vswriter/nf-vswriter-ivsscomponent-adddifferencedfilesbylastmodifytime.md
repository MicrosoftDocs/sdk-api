---
UID: NF:vswriter.IVssComponent.AddDifferencedFilesByLastModifyTime
title: IVssComponent::AddDifferencedFilesByLastModifyTime method
author: windows-driver-content
description: Used by a writer to indicate that a file set (a specified file or files) should be evaluated against a last modification time stamp for inclusion in a time stamped incremental or differential backup using entire files.
old-location: base\ivsscomponent_adddifferencedfilesbylastmodifytime.htm
old-project: VSS
ms.assetid: 33372d10-c947-45de-9ea2-03ba6378179d
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: AddDifferencedFilesByLastModifyTime method [VSS], AddDifferencedFilesByLastModifyTime method [VSS], IVssComponent interface, AddDifferencedFilesByLastModifyTime,IVssComponent.AddDifferencedFilesByLastModifyTime, IVssComponent, IVssComponent interface [VSS], AddDifferencedFilesByLastModifyTime method, IVssComponent::AddDifferencedFilesByLastModifyTime, _win32_ivsscomponent_adddifferencedfilesbylastmodifytime, base.ivsscomponent_adddifferencedfilesbylastmodifytime, vswriter/IVssComponent::AddDifferencedFilesByLastModifyTime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: VSS_WRITERRESTORE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	VssApi.lib
-	VssApi.dll
api_name:
-	IVssComponent.AddDifferencedFilesByLastModifyTime
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssComponent::AddDifferencedFilesByLastModifyTime method


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
       <a href="https://msdn.microsoft.com/d0e08598-a8a2-489b-9cb2-e989bed1ce53">Working with Mounted Folders and Reparse Points</a>.


### -param ftLastModifyTime [in]

The writer specification of the time of last modification for the difference files, expressed as a 
      <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure.
      

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
        <a href="vssgloss_b.htm">BackupComplete</a> or 
        <a href="vssgloss_b.htm">BackupShutdown</a> event.

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
        <a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.

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
        <a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
</table>
 




## -remarks



A writer calls this method to specify that certain files in a component should be backed up only if they have been modified since a certain time. For more information, see <a href="writer_role_in_backing_up_complex_stores.htm">Backup By Last Modify Time</a>.

This method can be called only by writers supporting the last modified schema 
    (<b>VSS_BS_LAST_MODIFY</b>), and only during backup operations. Writers using this method do 
    not have to support the time-stamp schema (<b>VSS_BS_TIMESTAMPED</b>).

Files added by 
    <b>AddDifferencedFilesByLastModifyTime</b> 
    should not also be added by 
    <a href="https://msdn.microsoft.com/318dc1ee-e63f-4e79-96b9-8a8bd83facd3">IVssComponent::AddPartialFile</a>.

If the backup type (<a href="https://msdn.microsoft.com/82934737-0d80-4b5d-a1fa-1ba38e446504">VSS_BACKUP_TYPE</a>) is incremental 
    (<b>VSS_BT_INCREMENTAL</b>), writers using 
    <b>AddDifferencedFilesByLastModifyTime</b> 
    must support the incremental schema (<b>VSS_BS_INCREMENTAL</b>). If the backup type is 
    differential, the writer must support the <b>VSS_BS_DIFFERENTIAL</b> schema.

The 
    <b>AddDifferencedFilesByLastModifyTime</b> 
    method should be called prior to the actual start of a backup operation, typically while handling the 
    <a href="vssgloss_p.htm">PostSnapshot</a> event (see 
    <a href="https://msdn.microsoft.com/d97d4246-882e-49c3-a214-d8d3887c1508">CVssWriter::OnPostSnapshot</a>).

If the time-stamp value set by 
    <b>AddDifferencedFilesByLastModifyTime</b> 
    is nonzero, a requester must respect this value regardless of its own records and file system information when 
    determining if the differenced file should be included in a differential or incremental backup.

If the time stamp set by 
    <b>AddDifferencedFilesByLastModifyTime</b> 
    (<i>ftLastModifyTime</i>) is zero, the requester can use file system information and its own 
    records to determine whether the differenced files should be included in a differential or incremental backup.

Requesters retrieve the number of differenced files managed by a component by calling 
    <a href="https://msdn.microsoft.com/285b2ac7-d09e-4ac5-bf5c-62c510544353">IVssComponent::GetDifferencedFile</a>.

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
    <a href="https://msdn.microsoft.com/5d5a0155-467c-4c42-876e-a1b245cf6f8e">IVssCreateWriterMetadata::AddFilesToFileGroup</a>, 
    <a href="https://msdn.microsoft.com/37ef5e50-127d-4bd0-9d26-04dc7781b3ff">IVssCreateWriterMetadata::AddDatabaseFiles</a>, or 
    <a href="https://msdn.microsoft.com/09bdbdf3-d757-4d3c-8b8b-f792b6cd4ef1">IVssCreateWriterMetadata::AddDatabaseLogFiles</a>.

When adding new files to the component, 
    <b>AddDifferencedFilesByLastModifyTime</b>, 
    the writer should not add files managed by another component or writer.

There is no method in the 
    <a href="https://msdn.microsoft.com/c686a424-b0b9-4efc-8dc6-b92193de2a5d">IVssComponent</a> interface that allows for changing or adding 
    an alternate location mappings for new files added by 
    <b>AddDifferencedFilesByLastModifyTime</b>. 
    If an alternate location mapping corresponds to the new file, then that alternate location will be used.




## -see-also




<a href="https://msdn.microsoft.com/d97d4246-882e-49c3-a214-d8d3887c1508">CVssWriter::OnPostSnapshot</a>



<a href="https://msdn.microsoft.com/c686a424-b0b9-4efc-8dc6-b92193de2a5d">IVssComponent</a>



<a href="https://msdn.microsoft.com/285b2ac7-d09e-4ac5-bf5c-62c510544353">IVssComponent::GetDifferencedFile</a>



<a href="https://msdn.microsoft.com/46faeb2b-7d83-4618-ba36-bdacc5ca055d">IVssComponent::GetDifferencedFilesCount</a>



<a href="https://msdn.microsoft.com/e9529aad-cf93-4b4c-811c-0ff0b708de6c">Incremental and Differential Backups</a>



<a href="https://msdn.microsoft.com/3541c8bd-2712-458b-9153-1fffe6bf5688">VSS_BACKUP_SCHEMA</a>



<a href="https://msdn.microsoft.com/82934737-0d80-4b5d-a1fa-1ba38e446504">VSS_BACKUP_TYPE</a>



<a href="https://msdn.microsoft.com/41ba60f7-d621-478a-a24a-202d326ebf2c">VSS_FILE_SPEC_BACKUP_TYPE</a>
 

 

