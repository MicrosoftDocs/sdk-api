---
UID: NF:vswriter.IVssCreateWriterMetadata.SetBackupSchema
title: IVssCreateWriterMetadata::SetBackupSchema (vswriter.h)
description: The SetBackupSchema method is used by a writer to indicate in its Writer Metadata Document the types of backup operations it can participate in.
helpviewer_keywords: ["IVssCreateWriterMetadata interface [VSS]","SetBackupSchema method","IVssCreateWriterMetadata.SetBackupSchema","IVssCreateWriterMetadata::SetBackupSchema","SetBackupSchema","SetBackupSchema method [VSS]","SetBackupSchema method [VSS]","IVssCreateWriterMetadata interface","_win32_ivsscreatewritermetadata_setbackupschema","base.ivsscreatewritermetadata_setbackupschema","vswriter/IVssCreateWriterMetadata::SetBackupSchema"]
old-location: base\ivsscreatewritermetadata_setbackupschema.htm
tech.root: base
ms.assetid: 7449fcc8-76fc-4cc5-923c-9a5d53d2cd6b
ms.date: 12/05/2018
ms.keywords: IVssCreateWriterMetadata interface [VSS],SetBackupSchema method, IVssCreateWriterMetadata.SetBackupSchema, IVssCreateWriterMetadata::SetBackupSchema, SetBackupSchema, SetBackupSchema method [VSS], SetBackupSchema method [VSS],IVssCreateWriterMetadata interface, _win32_ivsscreatewritermetadata_setbackupschema, base.ivsscreatewritermetadata_setbackupschema, vswriter/IVssCreateWriterMetadata::SetBackupSchema
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
 - IVssCreateWriterMetadata::SetBackupSchema
 - vswriter/IVssCreateWriterMetadata::SetBackupSchema
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
 - IVssCreateWriterMetadata.SetBackupSchema
---

# IVssCreateWriterMetadata::SetBackupSchema


## -description

The 
<b>SetBackupSchema</b> method is used by a writer to indicate in its Writer Metadata Document the types of backup operations it can participate in.

## -parameters

### -param dwSchemaMask [in]

The types of backup operations this writer supports expressed as a bitmask of 
<a href="/windows/desktop/api/vss/ne-vss-vss_backup_schema">VSS_BACKUP_SCHEMA</a> enumeration values.

For express writers, only the <b>VSS_BS_UNDEFINED</b>, <b>VSS_BS_COPY</b>, and <b>VSS_BS_INDEPENDENT_SYSTEM_STATE</b> values are supported.

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
Successfully set the failure message.

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
The backup schema argument is not valid.

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
The caller specified a <a href="/windows/desktop/api/vss/ne-vss-vss_backup_schema">VSS_BACKUP_SCHEMA</a> value that is not supported for express writers.

</td>
</tr>
</table>

## -remarks

If no schema is explicitly set by 
<b>SetBackupSchema</b>, the writer will be assigned the default value of VSS_BS_UNDEFINED: the writer supports only simple full backup and restoration of entire files (as defined by VSS_BT_FULL), there is no support for incremental or differential backups, and partial files are not supported.

Requesters call 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema">IVssExamineWriterMetadata::GetBackupSchema</a> to retrieve a writer's backup schemas as set by 
<b>SetBackupSchema</b>.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscreatewritermetadata">IVssCreateWriterMetadata</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema">IVssExamineWriterMetadata::GetBackupSchema</a>



<a href="/windows/desktop/api/vss/ne-vss-vss_backup_schema">VSS_BACKUP_SCHEMA</a>