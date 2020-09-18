---
UID: NF:vsbackup.IVssBackupComponents.GatherWriterMetadata
title: IVssBackupComponents::GatherWriterMetadata (vsbackup.h)
description: The GatherWriterMetadata method prompts each writer to send the metadata they have collected. The method will generate an Identify event to communicate with writers.
helpviewer_keywords: ["GatherWriterMetadata","GatherWriterMetadata method [VSS]","GatherWriterMetadata method [VSS]","IVssBackupComponents interface","IVssBackupComponents interface [VSS]","GatherWriterMetadata method","IVssBackupComponents.GatherWriterMetadata","IVssBackupComponents::GatherWriterMetadata","_win32_ivssbackupcomponents_gatherwritermetadata","base.ivssbackupcomponents_gatherwritermetadata","vsbackup/IVssBackupComponents::GatherWriterMetadata"]
old-location: base\ivssbackupcomponents_gatherwritermetadata.htm
tech.root: base
ms.assetid: 44f19c10-c966-4ab6-98dd-865d535955db
ms.date: 12/05/2018
ms.keywords: GatherWriterMetadata, GatherWriterMetadata method [VSS], GatherWriterMetadata method [VSS],IVssBackupComponents interface, IVssBackupComponents interface [VSS],GatherWriterMetadata method, IVssBackupComponents.GatherWriterMetadata, IVssBackupComponents::GatherWriterMetadata, _win32_ivssbackupcomponents_gatherwritermetadata, base.ivssbackupcomponents_gatherwritermetadata, vsbackup/IVssBackupComponents::GatherWriterMetadata
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
 - IVssBackupComponents::GatherWriterMetadata
 - vsbackup/IVssBackupComponents::GatherWriterMetadata
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
 - IVssBackupComponents.GatherWriterMetadata
---

# IVssBackupComponents::GatherWriterMetadata


## -description

The 
<b>GatherWriterMetadata</b> method prompts each writer to send the metadata they have collected. The method will generate an <a href="/windows/desktop/VSS/vssgloss-i">Identify</a> event to communicate with writers.

## -parameters

### -param pAsync [out]

Doubly indirect pointer to an 
<a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a> object containing the writer metadata.

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
Successfully returned a pointer to an instance of the 
<a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a> interface. See 
<a href="/windows/desktop/api/vss/nf-vss-ivssasync-querystatus">IVssAsync::QueryStatus</a> for the valid values returned by the <i>pHrResult</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient backup privileges or is not an administrator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppAsync</i> does not point to a valid pointer; that is, it is <b>NULL</b>.

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
<dt><b>VSS_E_WRITER_INFRASTRUCTURE</b></dt>
</dl>
</td>
<td width="60%">
The writer infrastructure is not operating properly. Check that the Event Service and VSS have been started, and check for errors associated with those services in the error log.

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

The caller is responsible for releasing the 
<a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a> interface.

<b>GatherWriterMetadata</b> should be called only once during the lifetime of a given 
<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a> object.

<b>GatherWriterMetadata</b> generates an Identify event, which is handled by each instance of each writer through the 
<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onidentify">CVssWriter::OnIdentify</a> method, which is used to fill the Writer Metadata Document.

## -see-also

<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onidentify">CVssWriter::OnIdentify</a>



<a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a>



<a href="/windows/desktop/api/vss/nf-vss-ivssasync-querystatus">IVssAsync::QueryStatus</a>



<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>