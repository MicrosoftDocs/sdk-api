---
UID: NF:vsbackup.IVssBackupComponents.GetWriterMetadataCount
title: IVssBackupComponents::GetWriterMetadataCount (vsbackup.h)
description: The GetWriterMetadataCount method returns the number of writers with metadata.
helpviewer_keywords: ["GetWriterMetadataCount","GetWriterMetadataCount method [VSS]","GetWriterMetadataCount method [VSS]","IVssBackupComponents interface","IVssBackupComponents interface [VSS]","GetWriterMetadataCount method","IVssBackupComponents.GetWriterMetadataCount","IVssBackupComponents::GetWriterMetadataCount","_win32_ivssbackupcomponents_getwritermetadatacount","base.ivssbackupcomponents_getwritermetadatacount","vsbackup/IVssBackupComponents::GetWriterMetadataCount"]
old-location: base\ivssbackupcomponents_getwritermetadatacount.htm
tech.root: base
ms.assetid: cf8c4782-2850-4847-a7a1-95bd2bd547a1
ms.date: 12/05/2018
ms.keywords: GetWriterMetadataCount, GetWriterMetadataCount method [VSS], GetWriterMetadataCount method [VSS],IVssBackupComponents interface, IVssBackupComponents interface [VSS],GetWriterMetadataCount method, IVssBackupComponents.GetWriterMetadataCount, IVssBackupComponents::GetWriterMetadataCount, _win32_ivssbackupcomponents_getwritermetadatacount, base.ivssbackupcomponents_getwritermetadatacount, vsbackup/IVssBackupComponents::GetWriterMetadataCount
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
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
 - IVssBackupComponents::GetWriterMetadataCount
 - vsbackup/IVssBackupComponents::GetWriterMetadataCount
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
 - IVssBackupComponents.GetWriterMetadataCount
---

# IVssBackupComponents::GetWriterMetadataCount


## -description

The 
<b>GetWriterMetadataCount</b> method returns the number of writers with metadata.

## -parameters

### -param pcWriters [out]

Number of writers with metadata.

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
Successfully returned the number of writers with metadata.

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
<dt><b>VSS_E_BAD_STATE</b></dt>
</dl>
</td>
<td width="60%">
The backup components object is not initialized, this method has been called during a restore operation, or this method has not been called within the correct sequence.

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

A requester must call the asynchronous operation 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata">IVssBackupComponents::GatherWriterMetadata</a> and wait for it to complete prior to calling <b>IVssBackupComponents::GetWriterMetadataCount</b>.

The number of writers returned by 
<b>GetWriterMetadataCount</b> should always be the same as that returned by 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-getwriterstatuscount">IVssBackupComponents::GetWriterStatusCount</a>.

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata">IVssBackupComponents::GatherWriterMetadata</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata">IVssBackupComponents::GetWriterMetadata</a>



<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadata">IVssExamineWriterMetadata</a>