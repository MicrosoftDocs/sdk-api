---
UID: NF:vsbackup.IVssExamineWriterMetadata.GetBackupSchema
title: IVssExamineWriterMetadata::GetBackupSchema (vsbackup.h)
description: The GetBackupSchema method is used by a requester to determine from the Writer Metadata Document the types of backup operations that a given writer can participate in.
helpviewer_keywords: ["GetBackupSchema","GetBackupSchema method [VSS]","GetBackupSchema method [VSS]","IVssExamineWriterMetadata interface","IVssExamineWriterMetadata interface [VSS]","GetBackupSchema method","IVssExamineWriterMetadata.GetBackupSchema","IVssExamineWriterMetadata::GetBackupSchema","_win32_ivssexaminewritermetadata_getbackupschema","base.ivssexaminewritermetadata_getbackupschema","vsbackup/IVssExamineWriterMetadata::GetBackupSchema"]
old-location: base\ivssexaminewritermetadata_getbackupschema.htm
tech.root: base
ms.assetid: d7099d6e-b8dd-44a5-af68-f3347c5d251b
ms.date: 12/05/2018
ms.keywords: GetBackupSchema, GetBackupSchema method [VSS], GetBackupSchema method [VSS],IVssExamineWriterMetadata interface, IVssExamineWriterMetadata interface [VSS],GetBackupSchema method, IVssExamineWriterMetadata.GetBackupSchema, IVssExamineWriterMetadata::GetBackupSchema, _win32_ivssexaminewritermetadata_getbackupschema, base.ivssexaminewritermetadata_getbackupschema, vsbackup/IVssExamineWriterMetadata::GetBackupSchema
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
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
 - IVssExamineWriterMetadata::GetBackupSchema
 - vsbackup/IVssExamineWriterMetadata::GetBackupSchema
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
 - IVssExamineWriterMetadata.GetBackupSchema
---

# IVssExamineWriterMetadata::GetBackupSchema


## -description

The 
<b>GetBackupSchema</b> method is used by a requester to determine from the Writer Metadata Document the types of backup operations that a given writer can participate in.

## -parameters

### -param pdwSchemaMask

The types of backup operations that a given writer supports, expressed as a bit mask (or bitwise OR) of 
<a href="/windows/desktop/api/vss/ne-vss-vss_backup_schema">VSS_BACKUP_SCHEMA</a> enumeration values.

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
Successfully set the failure message.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The backup schema argument is not valid.

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
</table>

## -remarks

The default backup schema is VSS_BS_UNDEFINED: the writer supports only simple full backup and restoration of entire files (as defined by VSS_BT_FULL), there is no support for incremental or differential backups, and partial files are not supported.

The writer calls 
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema">IVssCreateWriterMetadata::SetBackupSchema</a> to indicate its supported schema in its Writer Metadata Document.

## -see-also

<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema">IVssCreateWriterMetadata::SetBackupSchema</a>



<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadata">IVssExamineWriterMetadata</a>



<a href="/windows/desktop/api/vss/ne-vss-vss_backup_schema">VSS_BACKUP_SCHEMA</a>