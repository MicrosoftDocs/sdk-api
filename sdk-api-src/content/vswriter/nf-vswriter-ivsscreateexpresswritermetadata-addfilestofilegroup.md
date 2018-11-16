---
UID: NF:vswriter.IVssCreateExpressWriterMetadata.AddFilesToFileGroup
title: IVssCreateExpressWriterMetadata::AddFilesToFileGroup
author: windows-sdk-content
description: Adds a file set (a specified file or files) to a specified file group component for an express writer.
old-location: base\ivsscreateexpresswritermetadata_addfilestofilegroup.htm
tech.root: VSS
ms.assetid: 9a3f409e-f58a-4c06-ad5e-b0a8bc03da2c
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AddFilesToFileGroup, AddFilesToFileGroup method, AddFilesToFileGroup method,IVssCreateExpressWriterMetadata interface, IVssCreateExpressWriterMetadata interface,AddFilesToFileGroup method, IVssCreateExpressWriterMetadata.AddFilesToFileGroup, IVssCreateExpressWriterMetadata::AddFilesToFileGroup, base.ivsscreateexpresswritermetadata_addfilestofilegroup, vswriter/IVssCreateExpressWriterMetadata::AddFilesToFileGroup
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssCreateExpressWriterMetadata.AddFilesToFileGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- vswriter.h
: 
- IVssCreateExpressWriterMetadata.AddFilesToFileGroup
: 
---

# IVssCreateExpressWriterMetadata::AddFilesToFileGroup


## -description


Adds a file set (a specified file or files) to a specified file group component for an express writer.


## -parameters




### -param wszLogicalPath [in]

A pointer to a <b>null</b>-terminated wide character string containing the logical path (which may be <b>NULL</b>) of the component to which to add the files. For more information, see <a href="https://msdn.microsoft.com/663c8ca9-8f5b-48bd-af2d-b2d90de9e492">Logical Pathing of Components</a>.


### -param wszGroupName [in]

A pointer to a <b>null</b>-terminated wide character string containing the name of the file group component. The type of this component must be VSS_CT_FILEGROUP; otherwise, the method will return an error.


### -param wszPath [in]

A pointer to a <b>null</b>-terminated wide character string containing the default root directory of the files to be added. 




The path can contain environment variables (for example, %SystemRoot%) but cannot contain wildcard characters.

There is no requirement that the path end with a backslash (\). It is up to applications that retrieve this information to check.


### -param wszFilespec [in]

A pointer to a <b>null</b>-terminated wide character string containing the file specification of the files to be included. 




A file specification cannot contain directory specifications (for example, no backslashes) but can contain the ? and * wildcard characters.


### -param bRecursive [in]

A Boolean value specifying whether the path specified by the <i>wszPath</i> parameter identifies only a single directory or if it indicates a hierarchy of directories to be traversed recursively. This parameter should be set to <b>true</b> if the path is treated as a hierarchy of directories to be recursed through, or <b>false</b> otherwise. 




For information on traversing over mounted folders, see 
<a href="https://msdn.microsoft.com/d0e08598-a8a2-489b-9cb2-e989bed1ce53">Working with Mounted Folders and Reparse Points</a>.


### -param wszAlternateLocation [in]

This parameter is reserved and must be <b>NULL</b>.


### -param dwBackupTypeMask [in]

A bitmask of 
<a href="https://msdn.microsoft.com/41ba60f7-d621-478a-a24a-202d326ebf2c">VSS_FILE_SPEC_BACKUP_TYPE</a> enumeration values to indicate if a writer should evaluate the file for participation in a certain type of backup operations. 


This parameter cannot include <b>VSS_FSBT_DIFFERENTIAL_BACKUP_REQUIRED</b>, <b>VSS_FSBT_INCREMENTAL_BACKUP_REQUIRED</b>, or <b>VSS_FSBT_LOG_BACKUP_REQUIRED</b>.

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
One of the parameter values is not valid, or the caller attempted to add file-group files to a non-file-group component.

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
<a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.

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
        <a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/49112cff-9e61-4218-a013-5ae5eb58b534">IVssCreateExpressWriterMetadata</a>
 

 

