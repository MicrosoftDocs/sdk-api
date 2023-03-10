---
UID: NF:vswriter.IVssCreateWriterMetadata.AddExcludeFiles
title: IVssCreateWriterMetadata::AddExcludeFiles (vswriter.h)
description: The AddExcludeFiles method is used to explicitly exclude a file set (a specified file or files) that might otherwise be implicitly included when a component of the current writer is backed up.
helpviewer_keywords: ["AddExcludeFiles","AddExcludeFiles method [VSS]","AddExcludeFiles method [VSS]","IVssCreateWriterMetadata interface","IVssCreateWriterMetadata interface [VSS]","AddExcludeFiles method","IVssCreateWriterMetadata.AddExcludeFiles","IVssCreateWriterMetadata::AddExcludeFiles","_win32_ivsscreatewritermetadata_addexcludefiles","base.ivsscreatewritermetadata_addexcludefiles","vswriter/IVssCreateWriterMetadata::AddExcludeFiles"]
old-location: base\ivsscreatewritermetadata_addexcludefiles.htm
tech.root: base
ms.assetid: 705bb666-9080-4b42-af58-9cc21fbf88cf
ms.date: 12/05/2018
ms.keywords: AddExcludeFiles, AddExcludeFiles method [VSS], AddExcludeFiles method [VSS],IVssCreateWriterMetadata interface, IVssCreateWriterMetadata interface [VSS],AddExcludeFiles method, IVssCreateWriterMetadata.AddExcludeFiles, IVssCreateWriterMetadata::AddExcludeFiles, _win32_ivsscreatewritermetadata_addexcludefiles, base.ivsscreatewritermetadata_addexcludefiles, vswriter/IVssCreateWriterMetadata::AddExcludeFiles
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
 - IVssCreateWriterMetadata::AddExcludeFiles
 - vswriter/IVssCreateWriterMetadata::AddExcludeFiles
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
 - IVssCreateWriterMetadata.AddExcludeFiles
---

# IVssCreateWriterMetadata::AddExcludeFiles


## -description

The 
<b>AddExcludeFiles</b> method is used to explicitly exclude a file set (a specified file or files) that might otherwise be implicitly included when a component of the current writer is backed up.

## -parameters

### -param wszPath [in]

Pointer to a null-terminated wide character string containing the root directory under which files are to be excluded. 




The directory can be a local directory on the VSS machine, or it can be a file share directory on a remote file server.

UNC paths are supported.

The path can contain environment variables (for example, %SystemRoot%) but cannot contain wildcard characters.

There is no requirement that the path end with a backslash ("\"). It is up to applications that retrieve this information to check.

### -param wszFilespec [in]

Pointer to a null-terminated wide character string containing the file specification of the files to be excluded. 




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

<b>Windows 7, Windows Server 2008 R2, Windows Vista, Windows Server 2008, Windows XP and Windows Server 2003:  </b>Remote file shares are not supported until Windows 8 and Windows Server 2012. Writers support only local resources—sets of files whose absolute path starts with a valid local volume specification and cannot be a mapped network drive. Therefore, path inputs (<i>wszPath</i>) to 
<b>AddExcludeFiles</b> (after the resolution of any environment variables) must be in this format.

For example, it is often convenient to define a component to include all files in a given directory and then use 
<b>AddExcludeFiles</b> to explicitly remove some files (for instance, temporary files) from a backup.

For more information on excluding files, see 
<a href="/windows/desktop/VSS/writer-metadata-document-contents">Exclude File List Specification</a>.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscreatewritermetadata">IVssCreateWriterMetadata</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-addcomponent">IVssCreateWriterMetadata::AddComponent</a>