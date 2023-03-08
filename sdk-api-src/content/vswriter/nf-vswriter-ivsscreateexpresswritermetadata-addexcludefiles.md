---
UID: NF:vswriter.IVssCreateExpressWriterMetadata.AddExcludeFiles
title: IVssCreateExpressWriterMetadata::AddExcludeFiles (vswriter.h)
description: Excludes a file set (a specified file or files) that might otherwise be implicitly included when a component of an express writer is backed up.
helpviewer_keywords: ["AddExcludeFiles","AddExcludeFiles method","AddExcludeFiles method","IVssCreateExpressWriterMetadata interface","IVssCreateExpressWriterMetadata interface","AddExcludeFiles method","IVssCreateExpressWriterMetadata.AddExcludeFiles","IVssCreateExpressWriterMetadata::AddExcludeFiles","base.ivsscreateexpresswritermetadata_addexcludefiles","vswriter/IVssCreateExpressWriterMetadata::AddExcludeFiles"]
old-location: base\ivsscreateexpresswritermetadata_addexcludefiles.htm
tech.root: base
ms.assetid: a8d0d6bc-456a-405e-abd9-5ab4b2a59e63
ms.date: 12/05/2018
ms.keywords: AddExcludeFiles, AddExcludeFiles method, AddExcludeFiles method,IVssCreateExpressWriterMetadata interface, IVssCreateExpressWriterMetadata interface,AddExcludeFiles method, IVssCreateExpressWriterMetadata.AddExcludeFiles, IVssCreateExpressWriterMetadata::AddExcludeFiles, base.ivsscreateexpresswritermetadata_addexcludefiles, vswriter/IVssCreateExpressWriterMetadata::AddExcludeFiles
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IVssCreateExpressWriterMetadata::AddExcludeFiles
 - vswriter/IVssCreateExpressWriterMetadata::AddExcludeFiles
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
 - IVssCreateExpressWriterMetadata.AddExcludeFiles
---

# IVssCreateExpressWriterMetadata::AddExcludeFiles


## -description

Excludes a file set (a specified file or files) that might otherwise be implicitly included when a component of an express writer is backed up.

## -parameters

### -param wszPath [in]

A pointer to a null-terminated wide character string containing the root directory under which files are to be excluded. 




The path can contain environment variables (for example, %SystemRoot%) but cannot contain wildcard characters.

There is no requirement that the path end with a backslash (\\). It is up to applications that retrieve this information to check.

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

Express writers support only local resources—sets of files whose absolute path starts with a valid local volume specification and cannot be a mapped network drive. Therefore, path inputs (<i>wszPath</i>) to 
<b>AddExcludeFiles</b> (after the resolution of any environment variables) must be in this format. For example, it is often convenient to define a component to include all files in a specified directory and then use 
<b>AddExcludeFiles</b> to explicitly remove some files (for instance, temporary files) from a backup.

For more information on excluding files, see 
<a href="/windows/desktop/VSS/writer-metadata-document-contents">Exclude File List Specification</a>.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscreateexpresswritermetadata">IVssCreateExpressWriterMetadata</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreateexpresswritermetadata-addcomponent">IVssCreateExpressWriterMetadata::AddComponent</a>