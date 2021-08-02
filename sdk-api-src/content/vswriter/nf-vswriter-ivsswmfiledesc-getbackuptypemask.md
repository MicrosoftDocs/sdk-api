---
UID: NF:vswriter.IVssWMFiledesc.GetBackupTypeMask
title: IVssWMFiledesc::GetBackupTypeMask (vswriter.h)
description: The GetBackupTypeMask method returns the file backup specification for the files specified by the current file descriptor as a bit mask (or bitwise OR) of VSS_FILE_SPEC_BACKUP_TYPE values.
helpviewer_keywords: ["GetBackupTypeMask","GetBackupTypeMask method [VSS]","GetBackupTypeMask method [VSS]","IVssWMFiledesc interface","IVssWMFiledesc interface [VSS]","GetBackupTypeMask method","IVssWMFiledesc.GetBackupTypeMask","IVssWMFiledesc::GetBackupTypeMask","base.ivsswmfiledesc_getbackuptypemask","vswriter/IVssWMFiledesc::GetBackupTypeMask"]
old-location: base\ivsswmfiledesc_getbackuptypemask.htm
tech.root: base
ms.assetid: 9d5f3a16-2053-42dd-867d-740c4a34bdb6
ms.date: 12/05/2018
ms.keywords: GetBackupTypeMask, GetBackupTypeMask method [VSS], GetBackupTypeMask method [VSS],IVssWMFiledesc interface, IVssWMFiledesc interface [VSS],GetBackupTypeMask method, IVssWMFiledesc.GetBackupTypeMask, IVssWMFiledesc::GetBackupTypeMask, base.ivsswmfiledesc_getbackuptypemask, vswriter/IVssWMFiledesc::GetBackupTypeMask
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
 - IVssWMFiledesc::GetBackupTypeMask
 - vswriter/IVssWMFiledesc::GetBackupTypeMask
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
 - IVssWMFiledesc.GetBackupTypeMask
---

# IVssWMFiledesc::GetBackupTypeMask


## -description

The <b>GetBackupTypeMask</b> method 
   returns the file backup specification for the files specified by the current file descriptor as a bit mask (or 
   bitwise OR) of <a href="/windows/desktop/api/vss/ne-vss-vss_file_spec_backup_type">VSS_FILE_SPEC_BACKUP_TYPE</a> values. 
   This information indicates if the files are to be evaluated by their writer for participation in various specific 
   types of backup operations (or if they will participate in an incremental or differential backups).

## -parameters

### -param pdwTypeMask

Pointer to a <b>DWORD</b> containing a bit mask (or bitwise OR) of 
      <a href="/windows/desktop/api/vss/ne-vss-vss_file_spec_backup_type">VSS_FILE_SPEC_BACKUP_TYPE</a> values indicating 
      the file backup specification for the file or file set described by the current 
      <a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswmfiledesc">IVssWMFiledesc</a> interface.

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

A file backup specification is specified by a writer when it adds a file specification to a component using the 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup">IVssCreateWriterMetadata::AddFilesToFileGroup</a>, 
   <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles">IVssCreateWriterMetadata::AddDatabaseFiles</a>, or 
   <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles">IVssCreateWriterMetadata::AddDatabaseLogFiles</a> method.

## -see-also

<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles">IVssCreateWriterMetadata::AddDatabaseFiles</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles">IVssCreateWriterMetadata::AddDatabaseLogFiles</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup">IVssCreateWriterMetadata::AddFilesToFileGroup</a>



<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswmfiledesc">IVssWMFiledesc</a>



<a href="/windows/desktop/api/vss/ne-vss-vss_file_spec_backup_type">VSS_FILE_SPEC_BACKUP_TYPE</a>