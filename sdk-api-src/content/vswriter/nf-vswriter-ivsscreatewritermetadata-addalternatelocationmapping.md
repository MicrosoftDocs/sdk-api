---
UID: NF:vswriter.IVssCreateWriterMetadata.AddAlternateLocationMapping
title: IVssCreateWriterMetadata::AddAlternateLocationMapping (vswriter.h)
description: The AddAlternateLocationMapping method creates an alternate location mapping for a file set.
helpviewer_keywords: ["AddAlternateLocationMapping","AddAlternateLocationMapping method [VSS]","AddAlternateLocationMapping method [VSS]","IVssCreateWriterMetadata interface","IVssCreateWriterMetadata interface [VSS]","AddAlternateLocationMapping method","IVssCreateWriterMetadata.AddAlternateLocationMapping","IVssCreateWriterMetadata::AddAlternateLocationMapping","_win32_ivsscreatewritermetadata_addalternatelocationmapping","base.ivsscreatewritermetadata_addalternatelocationmapping","vswriter/IVssCreateWriterMetadata::AddAlternateLocationMapping"]
old-location: base\ivsscreatewritermetadata_addalternatelocationmapping.htm
tech.root: base
ms.assetid: 966c40d4-8c19-43cc-ba49-028763478f49
ms.date: 12/05/2018
ms.keywords: AddAlternateLocationMapping, AddAlternateLocationMapping method [VSS], AddAlternateLocationMapping method [VSS],IVssCreateWriterMetadata interface, IVssCreateWriterMetadata interface [VSS],AddAlternateLocationMapping method, IVssCreateWriterMetadata.AddAlternateLocationMapping, IVssCreateWriterMetadata::AddAlternateLocationMapping, _win32_ivsscreatewritermetadata_addalternatelocationmapping, base.ivsscreatewritermetadata_addalternatelocationmapping, vswriter/IVssCreateWriterMetadata::AddAlternateLocationMapping
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
 - IVssCreateWriterMetadata::AddAlternateLocationMapping
 - vswriter/IVssCreateWriterMetadata::AddAlternateLocationMapping
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
 - IVssCreateWriterMetadata.AddAlternateLocationMapping
---

# IVssCreateWriterMetadata::AddAlternateLocationMapping


## -description

The 
<b>AddAlternateLocationMapping</b> method creates an alternate location mapping for a file set.

## -parameters

### -param wszSourcePath [in]

Null-terminated wide character string containing the name of the directory or directory hierarchy containing the files to be mapped. 




The directory can be a local directory on the VSS machine, or it can be a file share directory on a remote file server.

The path can contain environment variables (for example, %SystemRoot%) but cannot contain wildcard characters.

There is no requirement that the path end with a backslash ("\"). It is up to applications that retrieve this information to check.

### -param wszSourceFilespec [in]

Null-terminated wide character string containing the file specification of the files to be mapped. 




A file specification cannot contain directory specifications (for example, no backslashes) but can contain the ? and * wildcard characters.

### -param bRecursive [in]

A Boolean value specifying whether the path specified by the <i>wszPath</i> parameter identifies only a single directory or if it indicates a hierarchy of directories to be traversed recursively. This parameter should be set to  <b>true</b> if the path is treated as a hierarchy of directories to be traversed recursively, or <b>false</b> if not. 




For information on traversing mounted folders, see 
<a href="/windows/desktop/VSS/working-with-reparse-and-mount-points">Working with Mounted Folders and Reparse Points</a>.

### -param wszDestination [in]

Null-terminated wide character string containing the fully qualified path to the directory where the files will be relocated.

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
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
<dt>0x80042308L</dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod">IVssCreateWriterMetadata::SetRestoreMethod</a> method was not called before this method was called.

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

<b>Windows 7, Windows Server 2008 R2, Windows Vista, Windows Server 2008, Windows XP and Windows Server 2003:  </b>Remote file shares are not supported until Windows 8 and Windows Server 2012. Writers support only local resources—sets of files whose absolute path starts with a valid local volume specification and cannot be a mapped network drive. Therefore, path inputs (<i>wszPath</i> and <i>wszDestination</i>) to 
<b>AddAlternateLocationMapping</b> (after the resolution of any environment variables) must be in this format.

This method can be called multiple times to add mapping for multiple files.

The combination of path, file specification, and recursion flag (<i>wszPath</i>, <i>wszFileSpec</i>, and <i>bRecursive</i>, respectively) provided to 
<b>AddAlternateLocationMapping</b> to be mapped must match that of one of the file sets added to one of the writer's components using 
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup">IVssCreateWriterMetadata::AddFilesToFileGroup</a>, 
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles">IVssCreateWriterMetadata::AddDatabaseFiles</a>, or 
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles">IVssCreateWriterMetadata::AddDatabaseLogFiles</a>.

The 
<b>AddAlternateLocationMapping</b> method should be called only after 
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod">IVssCreateWriterMetadata::SetRestoreMethod</a> is called.

A file should always be restored to its alternate location mapping if either of the following is true:

<ul>
<li>The restore method (set at backup time) is VSS_RME_RESTORE_TO_ALTERNATE_LOCATION.</li>
<li>Its restore target was set (at restore time) to VSS_RT_ALTERNATE.</li>
</ul>
In either case, if no valid alternate location mapping is defined, this constitutes a writer error.

A file can be restored to an alternate location mapping if either of the following is true:

<ul>
<li>The restore method is VSS_RME_RESTORE_IF_NOT_THERE and a version of the file is already present on disk.</li>
<li>The restore method is VSS_RME_RESTORE_IF_CAN_REPLACE and a version of the file is present on disk and cannot be replaced.</li>
</ul>
Again, if no valid alternate location mapping is defined, this constitutes a writer error.

An alternate location mapping is used only during a restore operation and should not be confused with an alternate path, which is used only during a backup operation.

For more information on backup and restore file locations under VSS, see 
<a href="/windows/desktop/VSS/non-default-backup-and-restore-locations">Non-Default Backup And Restore Locations</a>.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscreatewritermetadata">IVssCreateWriterMetadata</a>