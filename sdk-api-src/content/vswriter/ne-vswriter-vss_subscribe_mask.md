---
UID: NE:vswriter.VSS_SUBSCRIBE_MASK
title: VSS_SUBSCRIBE_MASK
author: windows-driver-content
description: Indicates the events that the writer is willing to receive.
old-location: base\vss_subscribe_mask.htm
old-project: VSS
ms.assetid: 4aa3afe4-98da-4376-b795-75bf404aaed9
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: VSS_SM_ALL_FLAGS, VSS_SM_BACKUP_EVENTS_FLAG, VSS_SM_IO_THROTTLING_FLAG, VSS_SM_POST_SNAPSHOT_FLAG, VSS_SM_RESTORE_EVENTS_FLAG, VSS_SUBSCRIBE_MASK, VSS_SUBSCRIBE_MASK enumeration [VSS], _win32_vss_subscribe_mask, base.vss_subscribe_mask, enumeration [VSS], vswriter/VSS_SM_ALL_FLAGS, vswriter/VSS_SM_BACKUP_EVENTS_FLAG, vswriter/VSS_SM_IO_THROTTLING_FLAG, vswriter/VSS_SM_POST_SNAPSHOT_FLAG, vswriter/VSS_SM_RESTORE_EVENTS_FLAG, vswriter/VSS_SUBSCRIBE_MASK
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: VSS_SUBSCRIBE_MASK
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	VsWriter.h
api_name:
-	VSS_SUBSCRIBE_MASK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# VSS_SUBSCRIBE_MASK enumeration


## -description


The <b>VSS_SUBSCRIBE_MASK</b> enumeration is used by a 
    writer when subscribing to the VSS service. It indicates the events that the writer is willing to 
    receive.


## -enum-fields




### -field VSS_SM_POST_SNAPSHOT_FLAG

This enumeration value is reserved for future use. 
      

Specifies that the writer expects to be notified after the shadow copy it is participating in has completed. 
       It will then call 
       <a href="https://msdn.microsoft.com/d97d4246-882e-49c3-a214-d8d3887c1508">CVssWriter::OnPostSnapshot</a>.


### -field VSS_SM_BACKUP_EVENTS_FLAG

Currently, <b>VSS_SM_BACKUP_EVENTS_FLAG</b> can be used as an argument only when 
      combined through a bitwise OR with <b>VSS_SM_RESTORE_EVENTS_FLAG</b>. 
      

Specifies that the writer can expect to receive the following events:

<ul>
<li>A PrepareForSnapshot event when the writer will call 
        <a href="https://msdn.microsoft.com/a077323e-d04c-4bf7-8aa6-5028fa1c6e6b">CVssWriter::OnPrepareSnapshot</a>.</li>
<li>A PrepareForBackup event when the writer will call 
        <a href="https://msdn.microsoft.com/4e88d92b-48f3-42f9-bf66-61337a745902">CVssWriter::OnPrepareBackup</a>.</li>
<li>A Freeze event when the writer will call 
        <a href="https://msdn.microsoft.com/2aff5e87-4053-46a0-a7fb-7411e76166ba">CVssWriter::OnFreeze</a>.</li>
<li>A BackupComplete event when the writer will call 
        <a href="https://msdn.microsoft.com/77d0621d-81bd-4d53-8e5d-f5d3bfd86013">CVssWriter::OnBackupComplete</a>.</li>
<li>A Thaw event when the writer will call 
        <a href="https://msdn.microsoft.com/36028e9f-f7a7-41f1-a570-48f943e9ab83">CVssWriter::OnThaw</a>.</li>
<li>A PostSnapshot event when the writer will call 
        <a href="https://msdn.microsoft.com/d97d4246-882e-49c3-a214-d8d3887c1508">CVssWriter::OnPostSnapshot</a>.</li>
</ul>

### -field VSS_SM_RESTORE_EVENTS_FLAG

Currently, <b>VSS_SM_RESTORE_EVENTS_FLAG</b> can be used as an argument only when 
      combined through a bitwise OR with <b>VSS_SM_BACKUP_EVENTS_FLAG</b>. 
      

Specifies that the writer can expect to receive the following events:

<ul>
<li>A PreRestore event when the writer will call 
        <a href="https://msdn.microsoft.com/5f4a6168-4102-4790-81d6-d195a440471f">CVssWriter::OnPreRestore</a>.</li>
<li>A PostRestore event when the writer will call 
        <a href="https://msdn.microsoft.com/ad07753c-1592-4fc8-9899-a73e798c158c">CVssWriter::OnPostRestore</a>.</li>
</ul>

### -field VSS_SM_IO_THROTTLING_FLAG

This enumeration value is reserved for future use.


### -field VSS_SM_ALL_FLAGS

This enumeration value is reserved for future use. 
      

Specifies that the writer expects to be notified for all events.


## -remarks



A bit mask (or bitwise OR) of <b>VSS_SUBSCRIBE_MASK</b> 
    values is used as an argument only to 
    <a href="https://msdn.microsoft.com/ab9520c9-bd6b-4c81-87fc-f5cda6ee9c94">CVssWriter::Subscribe</a>.

Currently, the only supported <b>VSS_SUBSCRIBE_MASK</b> 
    bit mask is ( <b>VSS_SM_BACKUP_EVENTS_FLAG</b> | 
    <b>VSS_SM_RESTORE_EVENTS_FLAG</b>).




## -see-also




<a href="https://msdn.microsoft.com/64aaae49-1d78-48ba-a38f-cab2ef2c4271">CVssWriter::OnBackOffIOOnVolume</a>



<a href="https://msdn.microsoft.com/77d0621d-81bd-4d53-8e5d-f5d3bfd86013">CVssWriter::OnBackupComplete</a>



<a href="https://msdn.microsoft.com/dd8271a3-4119-412d-abbd-1251196ac948">CVssWriter::OnContinueIOOnVolume</a>



<a href="https://msdn.microsoft.com/ad07753c-1592-4fc8-9899-a73e798c158c">CVssWriter::OnPostRestore</a>



<a href="https://msdn.microsoft.com/d97d4246-882e-49c3-a214-d8d3887c1508">CVssWriter::OnPostSnapshot</a>



<a href="https://msdn.microsoft.com/5f4a6168-4102-4790-81d6-d195a440471f">CVssWriter::OnPreRestore</a>



<a href="https://msdn.microsoft.com/4e88d92b-48f3-42f9-bf66-61337a745902">CVssWriter::OnPrepareBackup</a>



<a href="https://msdn.microsoft.com/ab9520c9-bd6b-4c81-87fc-f5cda6ee9c94">CVssWriter::Subscribe</a>
 

 

