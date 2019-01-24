---
UID: NF:vswriter.IVssWMFiledesc.GetBackupTypeMask
title: IVssWMFiledesc::GetBackupTypeMask
author: windows-sdk-content
description: The GetBackupTypeMask method returns the file backup specification for the files specified by the current file descriptor as a bit mask (or bitwise OR) of VSS_FILE_SPEC_BACKUP_TYPE values.
old-location: base\ivsswmfiledesc_getbackuptypemask.htm
tech.root: VSS
ms.assetid: 9d5f3a16-2053-42dd-867d-740c4a34bdb6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetBackupTypeMask, GetBackupTypeMask method [VSS], GetBackupTypeMask method [VSS],IVssWMFiledesc interface, IVssWMFiledesc interface [VSS],GetBackupTypeMask method, IVssWMFiledesc.GetBackupTypeMask, IVssWMFiledesc::GetBackupTypeMask, base.ivsswmfiledesc_getbackuptypemask, vswriter/IVssWMFiledesc::GetBackupTypeMask
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
 - IVssWMFiledesc.GetBackupTypeMask
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVssWMFiledesc::GetBackupTypeMask


## -description


The <b>GetBackupTypeMask</b> method 
   returns the file backup specification for the files specified by the current file descriptor as a bit mask (or 
   bitwise OR) of <a href="https://msdn.microsoft.com/41ba60f7-d621-478a-a24a-202d326ebf2c">VSS_FILE_SPEC_BACKUP_TYPE</a> values. 
   This information indicates if the files are to be evaluated by their writer for participation in various specific 
   types of backup operations (or if they will participate in an incremental or differential backups).


## -parameters




### -param pdwTypeMask

Pointer to a <b>DWORD</b> containing a bit mask (or bitwise OR) of 
      <a href="https://msdn.microsoft.com/41ba60f7-d621-478a-a24a-202d326ebf2c">VSS_FILE_SPEC_BACKUP_TYPE</a> values indicating 
      the file backup specification for the file or file set described by the current 
      <a href="https://msdn.microsoft.com/0b86882d-af1b-4a09-8c25-5b806c9ca909">IVssWMFiledesc</a> interface.


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
Successfully returned the filespec information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pdwTypeMask</i> variable points to a <b>NULL</b> region of memory.

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



A file backup specification is specified by a writer when it adds a file specification to a component using the 
    <a href="https://msdn.microsoft.com/5d5a0155-467c-4c42-876e-a1b245cf6f8e">IVssCreateWriterMetadata::AddFilesToFileGroup</a>, 
   <a href="https://msdn.microsoft.com/37ef5e50-127d-4bd0-9d26-04dc7781b3ff">IVssCreateWriterMetadata::AddDatabaseFiles</a>, or 
   <a href="https://msdn.microsoft.com/09bdbdf3-d757-4d3c-8b8b-f792b6cd4ef1">IVssCreateWriterMetadata::AddDatabaseLogFiles</a>method.




## -see-also




<a href="https://msdn.microsoft.com/37ef5e50-127d-4bd0-9d26-04dc7781b3ff">IVssCreateWriterMetadata::AddDatabaseFiles</a>



<a href="https://msdn.microsoft.com/09bdbdf3-d757-4d3c-8b8b-f792b6cd4ef1">IVssCreateWriterMetadata::AddDatabaseLogFiles</a>



<a href="https://msdn.microsoft.com/5d5a0155-467c-4c42-876e-a1b245cf6f8e">IVssCreateWriterMetadata::AddFilesToFileGroup</a>



<a href="https://msdn.microsoft.com/0b86882d-af1b-4a09-8c25-5b806c9ca909">IVssWMFiledesc</a>



<a href="https://msdn.microsoft.com/41ba60f7-d621-478a-a24a-202d326ebf2c">VSS_FILE_SPEC_BACKUP_TYPE</a>
 

 

