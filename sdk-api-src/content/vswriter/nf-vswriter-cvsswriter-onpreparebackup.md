---
UID: NF:vswriter.CVssWriter.OnPrepareBackup
title: CVssWriter::OnPrepareBackup
author: windows-sdk-content
description: The OnPrepareBackup method is called by a writer following a PrepareForBackup event. This method is used to configure a writer's state and its components in preparation for a backup operation.
old-location: base\cvsswriter_onpreparebackup.htm
tech.root: VSS
ms.assetid: 4e88d92b-48f3-42f9-bf66-61337a745902
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CVssWriter interface [VSS],OnPrepareBackup method, CVssWriter.OnPrepareBackup, CVssWriter::OnPrepareBackup, OnPrepareBackup, OnPrepareBackup method [VSS], OnPrepareBackup method [VSS],CVssWriter interface, _win32_cvsswriter_onpreparebackup, base.cvsswriter_onpreparebackup, vswriter/CVssWriter::OnPrepareBackup
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - CVssWriter.OnPrepareBackup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- vswriter.h
: 
- CVssWriter.OnPrepareBackup
: 
---

# CVssWriter::OnPrepareBackup


## -description


The 
<b>OnPrepareBackup</b> method is called by a writer following a 
<a href="https://msdn.microsoft.com/46ce8282-a434-4b0b-b66e-40810052b34b">PrepareForBackup</a> event. This method is used to configure a writer's state and its components in preparation for a backup operation.

<b>OnPrepareBackup</b> is a virtual method. It is implemented by the 
<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a> base class, but can be overridden by derived classes.


## -parameters




### -param pComponent [in]

Pointer to an instantiation of an 
<a href="https://msdn.microsoft.com/e8ff2491-014c-43c7-bdce-99ed3b408605">IVssWriterComponents</a> object containing the contents of the Writer Metadata Document. The value of this parameter may be <b>NULL</b> if the requester does not support components (if 
<a href="https://msdn.microsoft.com/da84f1ab-8712-436f-8ae7-ba3d52a761c0">CVssWriter::AreComponentsSelected</a> returns <b>false</b>).


## -returns



As implemented by the base class, 
<b>OnPrepareBackup</b> always returns <b>true</b>.

Any other implementation of this method must return <b>true</b> except in the case of a fatal error.
      If a fatal error occurs, the method must call the <a href="https://msdn.microsoft.com/9fef9d77-dc0d-4ba0-a317-5c62355458f7">CVssWriter::SetWriterFailure</a> method to provide a description of the failure before returning <b>false</b>. If a nonfatal error occurs, the method should still call <b>SetWriterFailure</b> but return <b>true</b>. If the error is caused by a transient problem, the method should specify VSS_E_WRITERERROR_RETRYABLE in the call to <b>SetWriterFailure</b>.

  In all cases when a failure occurs, the method should write an event to the event log to report the exact reason for the failure.




## -remarks



The default implementation of this method by the 
<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a> base class returns <b>true</b> without performing any other operation.

<b>OnPrepareBackup</b> provides a writer an opportunity to more finely select what will be backed up.

Handling the <a href="vssgloss_p.htm">PrepareForBackup</a> event is the last opportunity for a writer to get access to metadata contained in the Backup Components Document prior to the shadow copy's creation.

Therefore, 
<b>OnPrepareBackup</b> provides an opportunity for the writer to make any final additions or updates to stored component information (using the 
<a href="https://msdn.microsoft.com/c686a424-b0b9-4efc-8dc6-b92193de2a5d">IVssComponent</a> interface). In particular, writer-specific metadata can be updated by 
<a href="https://msdn.microsoft.com/96d0a581-87a5-4f97-b23f-08e90a805de1">IVssComponent::SetBackupMetadata</a> or 
<a href="https://msdn.microsoft.com/2b329fa8-21ad-4de9-9857-52e14d51d429">IVssComponent::SetRestoreMetadata</a>.

In addition, while handling the <a href="vssgloss_p.htm">PrepareForSnapshot</a> event provides another opportunity in the life cycle of a VSS backup operation to perform time-consuming operations (such as synchronizing data across multiple sites), 
<b>OnPrepareBackup</b> provides a chance for the writer to start such an operation asynchronously. Tasks like these must be completed prior to the return of 
<a href="https://msdn.microsoft.com/a077323e-d04c-4bf7-8aa6-5028fa1c6e6b">CVssWriter::OnPrepareSnapshot</a>.

Writers should never throw an exception from this method or any other <b>CVssWriter(Ex)::On<i>Xxx</i></b> callback method.

A requester generates a 
<a href="https://msdn.microsoft.com/46ce8282-a434-4b0b-b66e-40810052b34b">PrepareForBackup</a> event, triggering a call to 
<b>OnPrepareBackup</b>, by calling 
<b>IVssBackupComponents::PrepareForBackup</b>.

If this method calls the <a href="https://msdn.microsoft.com/bea5ba9c-538b-453f-ae6d-12b94b8edeb6">CVssWriterEx2::GetSessionId</a>, <a href="https://msdn.microsoft.com/9fef9d77-dc0d-4ba0-a317-5c62355458f7">CVssWriter::SetWriterFailure</a>, or <a href="https://msdn.microsoft.com/c049a016-6546-4e72-90e8-46be8c2f7764">CVssWriterEx2::SetWriterFailureEx</a> method, it must do so in  the same thread that called this method. For more information, see 
<a href="writers.htm">Writer Event Handling</a>.




## -see-also




<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a>



<a href="https://msdn.microsoft.com/d97d4246-882e-49c3-a214-d8d3887c1508">CVssWriter::OnPostSnapshot</a>



<a href="https://msdn.microsoft.com/5f4a6168-4102-4790-81d6-d195a440471f">CVssWriter::OnPreRestore</a>



<a href="https://msdn.microsoft.com/9fef9d77-dc0d-4ba0-a317-5c62355458f7">CVssWriter::SetWriterFailure</a>



<a href="https://msdn.microsoft.com/e8ff2491-014c-43c7-bdce-99ed3b408605">IVssWriterComponents</a>
 

 

