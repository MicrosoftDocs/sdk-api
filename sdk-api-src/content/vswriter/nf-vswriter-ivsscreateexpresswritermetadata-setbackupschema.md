---
UID: NF:vswriter.IVssCreateExpressWriterMetadata.SetBackupSchema
title: IVssCreateExpressWriterMetadata::SetBackupSchema
author: windows-sdk-content
description: Used by an express writer to indicate in its Writer Metadata Document the types of backup operations it can participate in.
old-location: base\ivsscreateexpresswritermetadata_setbackupschema.htm
old-project: VSS
ms.assetid: b270424d-61e1-4984-a487-4dcb4e113985
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IVssCreateExpressWriterMetadata interface,SetBackupSchema method, IVssCreateExpressWriterMetadata.SetBackupSchema, IVssCreateExpressWriterMetadata::SetBackupSchema, SetBackupSchema, SetBackupSchema method, SetBackupSchema method,IVssCreateExpressWriterMetadata interface, base.ivsscreateexpresswritermetadata_setbackupschema, vswriter/IVssCreateExpressWriterMetadata::SetBackupSchema
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VSS_WRITERRESTORE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssCreateExpressWriterMetadata.SetBackupSchema
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssCreateExpressWriterMetadata::SetBackupSchema


## -description


Used by an express writer to indicate in its Writer Metadata Document the types of backup operations it can participate in.


## -parameters




### -param dwSchemaMask






#### - dsSchemaMask [in]

A bitmask of 
<a href="https://msdn.microsoft.com/3541c8bd-2712-458b-9153-1fffe6bf5688">VSS_BACKUP_SCHEMA</a> enumeration values that specify the types of backup operations this writer supports.


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



If no schema is explicitly set by 
<b>SetBackupSchema</b>, the express writer will be assigned the default value of <b>VSS_BS_UNDEFINED</b>. <b>VSS_BS_UNDEFINED</b> means that the writer supports only simple full backup and restoration of entire files (as defined by <b>VSS_BT_FULL</b>), there is no support for incremental or differential backups, and partial files are not supported. Only the <b>VSS_BS_UNDEFINED</b>, <b>VSS_BS_COPY</b> and <b>VSS_BS_INDEPENDENT_SYSTEM_STATE</b> backup schema types are supported by express writers.

Requesters call 
<a href="https://msdn.microsoft.com/d7099d6e-b8dd-44a5-af68-f3347c5d251b">IVssExamineWriterMetadata::GetBackupSchema</a> to retrieve a writer's backup schemas as set by 
<b>SetBackupSchema</b>.




## -see-also




<a href="https://msdn.microsoft.com/49112cff-9e61-4218-a013-5ae5eb58b534">IVssCreateExpressWriterMetadata</a>
 

 

