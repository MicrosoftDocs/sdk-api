---
UID: NF:vswriter.IVssCreateWriterMetadataEx.AddExcludeFilesFromSnapshot
title: IVssCreateWriterMetadataEx::AddExcludeFilesFromSnapshot (vswriter.h)
description: Reports any file sets that will be explicitly excluded by the writer when a shadow copy is created.
helpviewer_keywords: ["AddExcludeFilesFromSnapshot","AddExcludeFilesFromSnapshot method","AddExcludeFilesFromSnapshot method","IVssCreateWriterMetadataEx interface","IVssCreateWriterMetadataEx interface","AddExcludeFilesFromSnapshot method","IVssCreateWriterMetadataEx.AddExcludeFilesFromSnapshot","IVssCreateWriterMetadataEx::AddExcludeFilesFromSnapshot","base.ivsscreatewritermetadataex_addexcludefilesfromsnapshot","vswriter/IVssCreateWriterMetadataEx::AddExcludeFilesFromSnapshot"]
old-location: base\ivsscreatewritermetadataex_addexcludefilesfromsnapshot.htm
tech.root: base
ms.assetid: 6be4c63c-c36a-4ff4-92b7-63b69a030b86
ms.date: 12/05/2018
ms.keywords: AddExcludeFilesFromSnapshot, AddExcludeFilesFromSnapshot method, AddExcludeFilesFromSnapshot method,IVssCreateWriterMetadataEx interface, IVssCreateWriterMetadataEx interface,AddExcludeFilesFromSnapshot method, IVssCreateWriterMetadataEx.AddExcludeFilesFromSnapshot, IVssCreateWriterMetadataEx::AddExcludeFilesFromSnapshot, base.ivsscreatewritermetadataex_addexcludefilesfromsnapshot, vswriter/IVssCreateWriterMetadataEx::AddExcludeFilesFromSnapshot
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
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
 - IVssCreateWriterMetadataEx::AddExcludeFilesFromSnapshot
 - vswriter/IVssCreateWriterMetadataEx::AddExcludeFilesFromSnapshot
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
 - IVssCreateWriterMetadataEx.AddExcludeFilesFromSnapshot
---

# IVssCreateWriterMetadataEx::AddExcludeFilesFromSnapshot


## -description

Reports any <a href="/windows/desktop/VSS/vssgloss-f">file sets</a> that will be explicitly excluded by the writer when a shadow copy is created.

Calling this method does not cause the files to be excluded. The writer is responsible for deleting the files from the shadow copy in its <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostsnapshot">CVssWriter::OnPostSnapshot</a> method.

## -parameters

### -param wszPath [in]

A pointer to a null-terminated wide character string containing the root directory under which files are to be excluded. 




The directory can be a local directory on the VSS machine, or it can be a file share directory on a remote file server.

UNC paths are supported.

The path can contain environment variables (for example, %SystemRoot%) but cannot contain wildcard characters.

There is no requirement that the path end with a backslash ("\"). It is up to applications that retrieve this information to check whether the path ends with a backslash.

### -param wszFilespec [in]

A pointer to a null-terminated wide character string containing the file specification of the files to be excluded. 




A file specification cannot contain directory specifications (for example, no backslashes) but can contain the ? and * wildcard characters.

### -param bRecursive [in]

A Boolean value specifying whether the path specified by the <i>wszPath</i> parameter identifies only a single directory or if it indicates a hierarchy of directories to be traversed recursively. This parameter should be set to <b>true</b> if the path is treated as a hierarchy of directories to be recursed through, or <b>false</b> otherwise. 




For information on traversing over mounted folders, see 
<a href="/windows/desktop/VSS/working-with-reparse-and-mount-points">Working with Mounted Folders and Reparse Points</a>.

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
This method is not supported for express writers.

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

The use of the <b>AddExcludeFilesFromSnapshot</b> method is optional. Writers should use this method only for large files that change significantly between shadow copy operations.

This method is not a substitute for the <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles">IVssCreateWriterMetadata::AddExcludeFiles</a> method. Writers should continue to use the <b>AddExcludeFiles</b> method to report which <a href="/windows/desktop/VSS/vssgloss-f">file sets</a> are excluded from backup.

The caller is responsible for calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method to release the resources of the returned 
<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswmfiledesc">IVssWMFiledesc</a> object.

## -see-also

<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles">IVssCreateWriterMetadata::AddExcludeFiles</a>



<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscreatewritermetadataex">IVssCreateWriterMetadataEx</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadataex2-getexcludefromsnapshotcount">IVssExamineWriterMetadataEx2::GetExcludeFromSnapshotCount</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadataex2-getexcludefromsnapshotfile">IVssExamineWriterMetadataEx2::GetExcludeFromSnapshotFile</a>