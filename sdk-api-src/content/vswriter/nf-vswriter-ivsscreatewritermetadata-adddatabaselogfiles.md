---
UID: NF:vswriter.IVssCreateWriterMetadata.AddDatabaseLogFiles
title: IVssCreateWriterMetadata::AddDatabaseLogFiles (vswriter.h)
description: The AddDatabaseLogFiles method indicates the log files that are associated with a database to be backed up, as well as their location.
helpviewer_keywords: ["AddDatabaseLogFiles","AddDatabaseLogFiles method [VSS]","AddDatabaseLogFiles method [VSS]","IVssCreateWriterMetadata interface","IVssCreateWriterMetadata interface [VSS]","AddDatabaseLogFiles method","IVssCreateWriterMetadata.AddDatabaseLogFiles","IVssCreateWriterMetadata::AddDatabaseLogFiles","_win32_ivsscreatewritermetadata_adddatabaselogfiles","base.ivsscreatewritermetadata_adddatabaselogfiles","vswriter/IVssCreateWriterMetadata::AddDatabaseLogFiles"]
old-location: base\ivsscreatewritermetadata_adddatabaselogfiles.htm
tech.root: base
ms.assetid: 09bdbdf3-d757-4d3c-8b8b-f792b6cd4ef1
ms.date: 12/05/2018
ms.keywords: AddDatabaseLogFiles, AddDatabaseLogFiles method [VSS], AddDatabaseLogFiles method [VSS],IVssCreateWriterMetadata interface, IVssCreateWriterMetadata interface [VSS],AddDatabaseLogFiles method, IVssCreateWriterMetadata.AddDatabaseLogFiles, IVssCreateWriterMetadata::AddDatabaseLogFiles, _win32_ivsscreatewritermetadata_adddatabaselogfiles, base.ivsscreatewritermetadata_adddatabaselogfiles, vswriter/IVssCreateWriterMetadata::AddDatabaseLogFiles
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
 - IVssCreateWriterMetadata::AddDatabaseLogFiles
 - vswriter/IVssCreateWriterMetadata::AddDatabaseLogFiles
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
 - IVssCreateWriterMetadata.AddDatabaseLogFiles
---

# IVssCreateWriterMetadata::AddDatabaseLogFiles


## -description

The 
<b>AddDatabaseLogFiles</b> method indicates the log files that are associated with a database to be backed up, as well as their location.

## -parameters

### -param wszLogicalPath [in]

Pointer to a <b>null</b>-terminated wide character string containing the logical path of the database component to which the log files will be added. 


For more information, see <a href="/windows/desktop/VSS/logical-pathing-of-components">Logical Pathing of Components</a>.

A logical path is not required, and can be <b>NULL</b>.

### -param wszDatabaseName [in]

Pointer to a <b>null</b>-terminated wide character string containing the name of the database component associated with the log files. The type of this component must be VSS_CT_DATABASE; otherwise, the method will return an error.

### -param wszPath [in]

Pointer to a <b>null</b>-terminated wide character string containing the path of the directory containing the log files. 




The directory can be a local directory on the VSS machine, or it can be a file share directory on a remote file server.

UNC paths are supported.

The path can contain environment variables (for example, %SystemRoot%) but cannot contain wildcard characters.

There is no requirement that the path end with a backslash ("\"). It is up to applications that retrieve this information to check.

### -param wszFilespec [in]

Pointer to a <b>null</b>-terminated wide character string containing the file specification of the log file(s) associated with the database. 




A file specification cannot contain directory specifications (for example, no backslashes) but can contain the ? and * wildcard characters.

### -param dwBackupTypeMask [in]

A bit mask (or bitwise OR) of 
<a href="/windows/desktop/api/vss/ne-vss-vss_file_spec_backup_type">VSS_FILE_SPEC_BACKUP_TYPE</a> enumeration values to indicate if a writer should evaluate the file for participation in a certain type of backup operations. 




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
One of the parameter values is not valid, or the caller attempted to add database files to a non-database component.

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
<b>AddDatabaseLogFiles</b> (after the resolution of any environment variables) must be in this format.

This method can be called multiple times for a particular database component, which might be needed when several log files are stored on separate volumes.

The values of the <i>wszLogicalPath</i> and <i>wszDatabaseName</i> parameters should match those of one of the database components previously added with the 
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-addcomponent">IVssCreateWriterMetadata::AddComponent</a> method.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscreatewritermetadata">IVssCreateWriterMetadata</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-addcomponent">IVssCreateWriterMetadata::AddComponent</a>