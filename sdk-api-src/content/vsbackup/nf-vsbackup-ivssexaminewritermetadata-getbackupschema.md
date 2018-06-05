---
UID: NF:vsbackup.IVssExamineWriterMetadata.GetBackupSchema
title: IVssExamineWriterMetadata::GetBackupSchema
author: windows-sdk-content
description: The GetBackupSchema method is used by a requester to determine from the Writer Metadata Document the types of backup operations that a given writer can participate in.
old-location: base\ivssexaminewritermetadata_getbackupschema.htm
old-project: VSS
ms.assetid: d7099d6e-b8dd-44a5-af68-f3347c5d251b
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetBackupSchema, GetBackupSchema method [VSS], GetBackupSchema method [VSS],IVssExamineWriterMetadata interface, IVssExamineWriterMetadata interface [VSS],GetBackupSchema method, IVssExamineWriterMetadata.GetBackupSchema, IVssExamineWriterMetadata::GetBackupSchema, _win32_ivssexaminewritermetadata_getbackupschema, base.ivssexaminewritermetadata_getbackupschema, vsbackup/IVssExamineWriterMetadata::GetBackupSchema
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: AMVPSIZE, *LPAMVPSIZE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	VssApi.lib
-	VssApi.dll
api_name:
-	IVssExamineWriterMetadata.GetBackupSchema
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssExamineWriterMetadata::GetBackupSchema


## -description


The 
<b>GetBackupSchema</b> method is used by a requester to determine from the Writer Metadata Document the types of backup operations that a given writer can participate in.


## -parameters




### -param pdwSchemaMask






#### - pdsSchemaMask

The types of backup operations that a given writer supports, expressed as a bit mask (or bitwise OR) of 
<a href="https://msdn.microsoft.com/3541c8bd-2712-458b-9153-1fffe6bf5688">VSS_BACKUP_SCHEMA</a> enumeration values.


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
<a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.

</td>
</tr>
</table>
 




## -remarks



The default backup schema is VSS_BS_UNDEFINED: the writer supports only simple full backup and restoration of entire files (as defined by VSS_BT_FULL), there is no support for incremental or differential backups, and partial files are not supported.

The writer calls 
<a href="https://msdn.microsoft.com/7449fcc8-76fc-4cc5-923c-9a5d53d2cd6b">IVssCreateWriterMetadata::SetBackupSchema</a> to indicate its supported schema in its Writer Metadata Document.




## -see-also




<a href="https://msdn.microsoft.com/7449fcc8-76fc-4cc5-923c-9a5d53d2cd6b">IVssCreateWriterMetadata::SetBackupSchema</a>



<a href="https://msdn.microsoft.com/b3aa04d9-7299-4e3a-b092-d07f2de6eefe">IVssExamineWriterMetadata</a>



<a href="https://msdn.microsoft.com/3541c8bd-2712-458b-9153-1fffe6bf5688">VSS_BACKUP_SCHEMA</a>
 

 

