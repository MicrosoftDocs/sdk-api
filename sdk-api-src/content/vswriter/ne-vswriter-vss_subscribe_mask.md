---
UID: NE:vswriter.VSS_SUBSCRIBE_MASK
title: VSS_SUBSCRIBE_MASK (vswriter.h)
description: Indicates the events that the writer is willing to receive.
helpviewer_keywords: ["VSS_SM_ALL_FLAGS","VSS_SM_BACKUP_EVENTS_FLAG","VSS_SM_IO_THROTTLING_FLAG","VSS_SM_POST_SNAPSHOT_FLAG","VSS_SM_RESTORE_EVENTS_FLAG","VSS_SUBSCRIBE_MASK","VSS_SUBSCRIBE_MASK enumeration [VSS]","_win32_vss_subscribe_mask","base.vss_subscribe_mask","enumeration [VSS]","vswriter/VSS_SM_ALL_FLAGS","vswriter/VSS_SM_BACKUP_EVENTS_FLAG","vswriter/VSS_SM_IO_THROTTLING_FLAG","vswriter/VSS_SM_POST_SNAPSHOT_FLAG","vswriter/VSS_SM_RESTORE_EVENTS_FLAG","vswriter/VSS_SUBSCRIBE_MASK"]
old-location: base\vss_subscribe_mask.htm
tech.root: base
ms.assetid: 4aa3afe4-98da-4376-b795-75bf404aaed9
ms.date: 12/05/2018
ms.keywords: VSS_SM_ALL_FLAGS, VSS_SM_BACKUP_EVENTS_FLAG, VSS_SM_IO_THROTTLING_FLAG, VSS_SM_POST_SNAPSHOT_FLAG, VSS_SM_RESTORE_EVENTS_FLAG, VSS_SUBSCRIBE_MASK, VSS_SUBSCRIBE_MASK enumeration [VSS], _win32_vss_subscribe_mask, base.vss_subscribe_mask, enumeration [VSS], vswriter/VSS_SM_ALL_FLAGS, vswriter/VSS_SM_BACKUP_EVENTS_FLAG, vswriter/VSS_SM_IO_THROTTLING_FLAG, vswriter/VSS_SM_POST_SNAPSHOT_FLAG, vswriter/VSS_SM_RESTORE_EVENTS_FLAG, vswriter/VSS_SUBSCRIBE_MASK
req.header: vswriter.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: VSS_SUBSCRIBE_MASK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VSS_SUBSCRIBE_MASK
 - vswriter/VSS_SUBSCRIBE_MASK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VsWriter.h
api_name:
 - VSS_SUBSCRIBE_MASK
---

# VSS_SUBSCRIBE_MASK enumeration


## -description

The <b>VSS_SUBSCRIBE_MASK</b> enumeration is used by a 
    writer when subscribing to the VSS service. It indicates the events that the writer is willing to 
    receive.

## -enum-fields

### -field VSS_SM_POST_SNAPSHOT_FLAG:0x00000001

This enumeration value is reserved for future use. 
      

Specifies that the writer expects to be notified after the shadow copy it is participating in has completed. 
       It will then call 
       <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostsnapshot">CVssWriter::OnPostSnapshot</a>.

### -field VSS_SM_BACKUP_EVENTS_FLAG:0x00000002

Currently, <b>VSS_SM_BACKUP_EVENTS_FLAG</b> can be used as an argument only when 
      combined through a bitwise OR with <b>VSS_SM_RESTORE_EVENTS_FLAG</b>. 
      

Specifies that the writer can expect to receive the following events:

<ul>
<li>A PrepareForSnapshot event when the writer will call 
        <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpreparesnapshot">CVssWriter::OnPrepareSnapshot</a>.</li>
<li>A PrepareForBackup event when the writer will call 
        <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpreparebackup">CVssWriter::OnPrepareBackup</a>.</li>
<li>A Freeze event when the writer will call 
        <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onfreeze">CVssWriter::OnFreeze</a>.</li>
<li>A BackupComplete event when the writer will call 
        <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onbackupcomplete">CVssWriter::OnBackupComplete</a>.</li>
<li>A Thaw event when the writer will call 
        <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onthaw">CVssWriter::OnThaw</a>.</li>
<li>A PostSnapshot event when the writer will call 
        <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostsnapshot">CVssWriter::OnPostSnapshot</a>.</li>
</ul>

### -field VSS_SM_RESTORE_EVENTS_FLAG:0x00000004

Currently, <b>VSS_SM_RESTORE_EVENTS_FLAG</b> can be used as an argument only when 
      combined through a bitwise OR with <b>VSS_SM_BACKUP_EVENTS_FLAG</b>. 
      

Specifies that the writer can expect to receive the following events:

<ul>
<li>A PreRestore event when the writer will call 
        <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onprerestore">CVssWriter::OnPreRestore</a>.</li>
<li>A PostRestore event when the writer will call 
        <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostrestore">CVssWriter::OnPostRestore</a>.</li>
</ul>

### -field VSS_SM_IO_THROTTLING_FLAG:0x00000008

This enumeration value is reserved for future use.

### -field VSS_SM_ALL_FLAGS:0xffffffff

This enumeration value is reserved for future use. 
      

Specifies that the writer expects to be notified for all events.

## -remarks

A bit mask (or bitwise OR) of <b>VSS_SUBSCRIBE_MASK</b> 
    values is used as an argument only to 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-subscribe">CVssWriter::Subscribe</a>.

Currently, the only supported <b>VSS_SUBSCRIBE_MASK</b> 
    bit mask is ( <b>VSS_SM_BACKUP_EVENTS_FLAG</b> | 
    <b>VSS_SM_RESTORE_EVENTS_FLAG</b>).

## -see-also

<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onbackoffioonvolume">CVssWriter::OnBackOffIOOnVolume</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onbackupcomplete">CVssWriter::OnBackupComplete</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-oncontinueioonvolume">CVssWriter::OnContinueIOOnVolume</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostrestore">CVssWriter::OnPostRestore</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostsnapshot">CVssWriter::OnPostSnapshot</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onprerestore">CVssWriter::OnPreRestore</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpreparebackup">CVssWriter::OnPrepareBackup</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-subscribe">CVssWriter::Subscribe</a>
