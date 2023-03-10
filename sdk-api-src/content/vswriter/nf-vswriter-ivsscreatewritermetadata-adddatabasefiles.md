---
UID: NF:vswriter.IVssCreateWriterMetadata.AddDatabaseFiles
title: IVssCreateWriterMetadata::AddDatabaseFiles (vswriter.h)
description: The AddDatabaseFiles method indicates the file set (the specified file or files) that make up the database component to be backed up.
helpviewer_keywords: ["AddDatabaseFiles","AddDatabaseFiles method [VSS]","AddDatabaseFiles method [VSS]","IVssCreateWriterMetadata interface","IVssCreateWriterMetadata interface [VSS]","AddDatabaseFiles method","IVssCreateWriterMetadata.AddDatabaseFiles","IVssCreateWriterMetadata::AddDatabaseFiles","_win32_ivsscreatewritermetadata_adddatabasefiles","base.ivsscreatewritermetadata_adddatabasefiles","vswriter/IVssCreateWriterMetadata::AddDatabaseFiles"]
old-location: base\ivsscreatewritermetadata_adddatabasefiles.htm
tech.root: base
ms.assetid: 37ef5e50-127d-4bd0-9d26-04dc7781b3ff
ms.date: 12/05/2018
ms.keywords: AddDatabaseFiles, AddDatabaseFiles method [VSS], AddDatabaseFiles method [VSS],IVssCreateWriterMetadata interface, IVssCreateWriterMetadata interface [VSS],AddDatabaseFiles method, IVssCreateWriterMetadata.AddDatabaseFiles, IVssCreateWriterMetadata::AddDatabaseFiles, _win32_ivsscreatewritermetadata_adddatabasefiles, base.ivsscreatewritermetadata_adddatabasefiles, vswriter/IVssCreateWriterMetadata::AddDatabaseFiles
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
 - IVssCreateWriterMetadata::AddDatabaseFiles
 - vswriter/IVssCreateWriterMetadata::AddDatabaseFiles
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
 - IVssCreateWriterMetadata.AddDatabaseFiles
---

# IVssCreateWriterMetadata::AddDatabaseFiles


## -description

The 
<b>AddDatabaseFiles</b> method indicates the file set (the specified file or files) that make up the database component to be backed up.

## -parameters

### -param wszLogicalPath [in]

Pointer to a <b>null</b>-terminated wide character string containing the logical path of the component to which the database will be added. 


For more information, see <a href="/windows/desktop/VSS/logical-pathing-of-components">Logical Pathing of Components</a>.

A logical path is not required and can be <b>NULL</b>.

### -param wszDatabaseName [in]

Pointer to a <b>null</b>-terminated wide character string containing the name of the database. 




This name is required and must match the name of the component to which the database is being added.

### -param wszPath [in]

Pointer to a <b>null</b>-terminated wide character string containing the path of the directory containing the database file. 




The path can contain environment variables (for example, %SystemRoot%) but cannot contain wildcard characters. 

UNC paths are supported.

There is no requirement that the path end with a backslash ("\"). It is up to applications that retrieve this information to check.

### -param wszFilespec [in]

Pointer to a <b>null</b>-terminated wide character string containing the file specification of the file or files associated with the database. 




A file specification cannot contain directory specifications (for example, no backslashes) but can contain the ? and * wildcard characters.

### -param dwBackupTypeMask [in]

A bit mask (or bitwise OR) of 
<a href="/windows/desktop/api/vss/ne-vss-vss_file_spec_backup_type">VSS_FILE_SPEC_BACKUP_TYPE</a> enumeration values to indicate whether a writer should evaluate the file for participation in certain types of backup operations. 




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

<b>Windows 7, Windows Server 2008 R2, Windows Vista, Windows Server 2008, Windows XP and Windows Server 2003:  </b>Remote file shares are not supported until Windows 8 and Windows Server 2012. Writers support only local resources—sets of files whose absolute path starts with a valid local volume specification and cannot be a mapped network drive. Therefore, path inputs (<i>wszPath</i>) to 
<b>AddDatabaseFiles</b> (after the resolution of any environment variables) must be in this format.

This method can be called multiple times for a particular database. This is done when the database exists on files stored on separate volumes, as is possible with Microsoft SQL Server.

The values of the <i>wszLogicalPath</i> and <i>wszDatabaseName</i> parameters should match those of one of the database components previously added with the 
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-addcomponent">IVssCreateWriterMetadata::AddComponent</a> method.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscreatewritermetadata">IVssCreateWriterMetadata</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-addcomponent">IVssCreateWriterMetadata::AddComponent</a>