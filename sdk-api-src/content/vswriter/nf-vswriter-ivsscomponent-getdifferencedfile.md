---
UID: NF:vswriter.IVssComponent.GetDifferencedFile
title: IVssComponent::GetDifferencedFile (vswriter.h)
description: The GetDifferencedFile method returns information about a file set (a specified file or files) to participate in an incremental or differential backup or restore as a differenced file that is, backup and restores associated with it are to be implemented as if entire files are copied to and from backup media (as opposed to using partial files).
helpviewer_keywords: ["GetDifferencedFile","GetDifferencedFile method [VSS]","GetDifferencedFile method [VSS]","IVssComponent interface","IVssComponent interface [VSS]","GetDifferencedFile method","IVssComponent.GetDifferencedFile","IVssComponent::GetDifferencedFile","_win32_ivsscomponent_getdifferencedfile","base.ivsscomponent_getdifferencedfile","vswriter/IVssComponent::GetDifferencedFile"]
old-location: base\ivsscomponent_getdifferencedfile.htm
tech.root: base
ms.assetid: 285b2ac7-d09e-4ac5-bf5c-62c510544353
ms.date: 12/05/2018
ms.keywords: GetDifferencedFile, GetDifferencedFile method [VSS], GetDifferencedFile method [VSS],IVssComponent interface, IVssComponent interface [VSS],GetDifferencedFile method, IVssComponent.GetDifferencedFile, IVssComponent::GetDifferencedFile, _win32_ivsscomponent_getdifferencedfile, base.ivsscomponent_getdifferencedfile, vswriter/IVssComponent::GetDifferencedFile
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
 - IVssComponent::GetDifferencedFile
 - vswriter/IVssComponent::GetDifferencedFile
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
 - IVssComponent.GetDifferencedFile
---

# IVssComponent::GetDifferencedFile


## -description

The <b>GetDifferencedFile</b> method returns 
    information about a file set (a specified file or files) to participate in an incremental or differential backup 
    or restore as a differenced file—that is, backup and restores associated with it are to be 
    implemented as if entire files are copied to and from backup media (as opposed to using partial files).

This method can be called by a requester or a writer during backup or restore operations.

## -parameters

### -param iDifferencedFile [in]

Index number of the differenced file to be examined. The value of this parameter is an integer from 0 
      to <i>n</i>–1 inclusive, where <i>n</i> is the total number of differenced files 
      associated with a given component (and its subcomponents if it defines a component set). The value of 
      <i>n</i> is returned by 
      <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getdifferencedfilescount">IVssComponent::GetDifferencedFilesCount</a>.

### -param pbstrPath [out]

The address of a caller-allocated variable that receives a string containing the path to the differenced files.
      

Users of this method need to check to determine whether this path ends with a backslash 
       (\\).

### -param pbstrFilespec [out]

The address of a caller-allocated variable that receives a string containing the file specification of the differenced files.

### -param pbRecursive [out]

The address of a caller-allocated variable that receives a Boolean specifying whether the file specification for the differenced files should be 
      interpreted recursively. If <b>TRUE</b>, then the entire directory hierarchy will need to be searched for files 
      matching the file specification <i>pbstrFilespec</i> to find files to be handled as 
      differenced files during incremental or differential backups. If <b>FALSE</b>, only the root directory needs to be 
      searched.

### -param pbstrLsnString [out]

Reserved for future use.

### -param pftLastModifyTime [out]

The address of a caller-allocated variable that receives the writer specification of the time of last modification for the difference files, expressed as a 
      <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure.

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
Successfully returned the attribute value.

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
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No differenced file corresponding to the supplied index was found.

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
</table>

## -remarks

<b>GetDifferencedFile</b> can be called by 
    a requester or a writer during backup or restore operations.

If the call to <b>GetDifferencedFile</b> is successful, the caller is responsible for freeing the string that  is returned in the <i>pbstrPath</i> and  <i>pbstrFilespec</i> parameters by calling the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function.

As writers can indicate differenced files with calls to 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime">IVssComponent::AddDifferencedFilesByLastModifyTime</a> 
    at any time prior to the actual backing up of files, typically while handling a 
    <a href="/windows/desktop/VSS/vssgloss-p">PostSnapshot</a> event 
    (<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostsnapshot">CVssWriter::OnPostSnapshot</a>), during backups 
    <b>GetDifferencedFile</b> is not usefully 
    called prior to the return of 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset">IVssBackupComponents::DoSnapshotSet</a> 
    has successfully returned.

The time stamp returned by 
    <b>GetDifferencedFile</b> applies to all files 
    that match the returned path (<i>pbstrPath</i>) and file specification 
    (<i>pbstrFilespec</i>).

If the time-stamp value returned by 
    <b>GetDifferencedFile</b> 
    (<i>pftLastModifyTime</i>) is nonzero, a requester must respect this value regardless of its 
    own records and file system information and use it to determine whether the differenced file should be included in a 
    differential or incremental backup.

If the time stamp returned by 
    <b>GetDifferencedFile</b> is zero, the 
    requester can use file system information and its own records to determine whether the differenced files should be 
    included in a differential or incremental backup.

Differenced files can be either of the following:

<ul>
<li>Members of the current component or, if the component defines a component set, members of its subcomponents 
      that were added to the component using 
      <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup">IVssCreateWriterMetadata::AddFilesToFileGroup</a>, 
      <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles">IVssCreateWriterMetadata::AddDatabaseFiles</a>, or 
      <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles">IVssCreateWriterMetadata::AddDatabaseLogFiles</a>
</li>
<li>New files added to the component by 
     <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime">IVssComponent::AddDifferencedFilesByLastModifyTime</a>
</li>
</ul>
When referring to a file set that is already part of the component, the combination of path, file 
    specification, and recursion flag (<i>wszPath</i>, <i>wszFileSpec</i>, and 
    <i>bRecursive</i>, respectively) used when calling 
    <b>GetDifferencedFile</b> should match that of 
    a file set already in the component, or one of its subcomponents (if the component defines a component set).

When <b>GetDifferencedFile</b> returns a 
    differenced new file, that file's path (<i>pbstrPath</i>) should match or be beneath a path 
    already in the component, or one of its subcomponents (if the component defines a component set).

In addition, the files returned by 
    <b>GetDifferencedFile</b> should not already 
    be managed by component or writer.

If any of these criteria are violated, they constitute an error on the part of the writer and should be 
    reported.

There is no method in the 
    <a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a> interface that allows for changing or adding 
    an alternate location mapping for new files returned by 
    <b>GetDifferencedFilesByLastModifyTime</b>. If an alternate location mapping corresponds 
    to the new file, then that alternate location will be used.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime">IVssComponent::AddDifferencedFilesByLastModifyTime</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getdifferencedfilescount">IVssComponent::GetDifferencedFilesCount</a>



<a href="/windows/desktop/VSS/incremental-and-differential-backups">Incremental and Differential Backups</a>