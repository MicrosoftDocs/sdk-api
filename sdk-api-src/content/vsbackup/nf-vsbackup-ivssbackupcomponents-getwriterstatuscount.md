---
UID: NF:vsbackup.IVssBackupComponents.GetWriterStatusCount
title: IVssBackupComponents::GetWriterStatusCount (vsbackup.h)
description: The GetWriterStatusCount method returns the number of writers with status.
helpviewer_keywords: ["GetWriterStatusCount","GetWriterStatusCount method [VSS]","GetWriterStatusCount method [VSS]","IVssBackupComponents interface","IVssBackupComponents interface [VSS]","GetWriterStatusCount method","IVssBackupComponents.GetWriterStatusCount","IVssBackupComponents::GetWriterStatusCount","_win32_ivssbackupcomponents_getwriterstatuscount","base.ivssbackupcomponents_getwriterstatuscount","vsbackup/IVssBackupComponents::GetWriterStatusCount"]
old-location: base\ivssbackupcomponents_getwriterstatuscount.htm
tech.root: base
ms.assetid: e358cb2b-9b0f-47fb-a0ca-7bbbc6e49aff
ms.date: 12/05/2018
ms.keywords: GetWriterStatusCount, GetWriterStatusCount method [VSS], GetWriterStatusCount method [VSS],IVssBackupComponents interface, IVssBackupComponents interface [VSS],GetWriterStatusCount method, IVssBackupComponents.GetWriterStatusCount, IVssBackupComponents::GetWriterStatusCount, _win32_ivssbackupcomponents_getwriterstatuscount, base.ivssbackupcomponents_getwriterstatuscount, vsbackup/IVssBackupComponents::GetWriterStatusCount
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
 - IVssBackupComponents::GetWriterStatusCount
 - vsbackup/IVssBackupComponents::GetWriterStatusCount
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
 - IVssBackupComponents.GetWriterStatusCount
---

# IVssBackupComponents::GetWriterStatusCount


## -description

The 
<b>GetWriterStatusCount</b> method returns the number of writers with status.

## -parameters

### -param pcWriters [out]

The number of writers with status.

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
Successfully returned the number of writers with status.

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
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus">IVssBackupComponents::GatherWriterStatus</a> and wait for it to complete prior to calling <b>IVssBackupComponents::GetWriterStatusCount</b>.

The number of writers returned by 
<b>GetWriterStatusCount</b> should always be the same as that returned by 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount">IVssBackupComponents::GetWriterMetadataCount</a>.

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus">IVssBackupComponents::GatherWriterStatus</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus">IVssBackupComponents::GetWriterStatus</a>



<a href="/windows/desktop/api/vss/ne-vss-vss_writer_state">VSS_WRITER_STATE</a>