---
UID: NF:vswriter.CVssWriter.OnPreRestore
title: CVssWriter::OnPreRestore
author: windows-driver-content
description: The OnPreRestore method is called by a writer following a PreRestore event.
old-location: base\cvsswriter_onprerestore.htm
old-project: VSS
ms.assetid: 5f4a6168-4102-4790-81d6-d195a440471f
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: CVssWriter interface [VSS],OnPreRestore method, CVssWriter.OnPreRestore, CVssWriter::OnPreRestore, OnPreRestore, OnPreRestore method [VSS], OnPreRestore method [VSS],CVssWriter interface, _win32_cvsswriter_onprerestore, base.cvsswriter_onprerestore, vswriter/CVssWriter::OnPreRestore
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
req.typenames: VSS_WRITERRESTORE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	VssApi.lib
-	VssApi.dll
api_name:
-	CVssWriter.OnPreRestore
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# CVssWriter::OnPreRestore


## -description


The 
<b>OnPreRestore</b> method is called by a writer following a 
<a href="https://msdn.microsoft.com/7a4c8869-9655-49a7-818b-98a08103f4b4">PreRestore</a> event. This method is used to put the writer in a state to support the restore—for instance, taking database services offline—and to make modifications in the Backup Components Document of the requester that is restoring files (such as setting the restore target to override the original restore method).

<b>OnPreRestore</b> is a virtual method. It is implemented by the 
<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a> base class, but can be overridden by derived classes.


## -parameters




### -param pComponent [in]

Pointer to an instantiation of an 
<a href="https://msdn.microsoft.com/e8ff2491-014c-43c7-bdce-99ed3b408605">IVssWriterComponents</a> object containing those components associated with the current writer in the requester's Backup Components Document.


## -returns



As implemented by the base class, 
<b>OnPreRestore</b> always returns <b>true</b>.

Any other implementation of this method must return <b>true</b> except in the case of a fatal error.
      If a fatal error occurs, the method must call the <a href="https://msdn.microsoft.com/9fef9d77-dc0d-4ba0-a317-5c62355458f7">CVssWriter::SetWriterFailure</a> method to provide a description of the failure before returning <b>false</b>. If a nonfatal error occurs, the method should still call <b>SetWriterFailure</b> but return <b>true</b>. If the error is caused by a transient problem, the method should specify VSS_E_WRITERERROR_RETRYABLE in the call to <b>SetWriterFailure</b>.

  In all cases when a failure occurs, the method should write an event to the event log to report the exact reason for the failure.




## -remarks



The 
<a href="https://msdn.microsoft.com/7a4c8869-9655-49a7-818b-98a08103f4b4">PreRestore</a> event occurs before backed-up data is actually being restored. This is an opportunity for the writer to determine what is being restored.

The default implementation of this method by the 
<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a> base class returns <b>true</b> without performing any other operation.

This method enables the writer to determine what is being restored, to retrieve stored private metadata in the stored Backup Components Document, and to update that data.

Writers should never throw an exception from this method or any other <b>CVssWriter(Ex)::On<i>Xxx</i></b> callback method.

If this method calls the <a href="https://msdn.microsoft.com/bea5ba9c-538b-453f-ae6d-12b94b8edeb6">CVssWriterEx2::GetSessionId</a>, <a href="https://msdn.microsoft.com/9fef9d77-dc0d-4ba0-a317-5c62355458f7">CVssWriter::SetWriterFailure</a>, or <a href="https://msdn.microsoft.com/c049a016-6546-4e72-90e8-46be8c2f7764">CVssWriterEx2::SetWriterFailureEx</a> method, it must do so in  the same thread that called this method. For more information, see 
<a href="writers.htm">Writer Event Handling</a>.




## -see-also




<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a>



<a href="https://msdn.microsoft.com/d97d4246-882e-49c3-a214-d8d3887c1508">CVssWriter::OnPostSnapshot</a>



<a href="https://msdn.microsoft.com/4e88d92b-48f3-42f9-bf66-61337a745902">CVssWriter::OnPrepareBackup</a>



<a href="https://msdn.microsoft.com/9fef9d77-dc0d-4ba0-a317-5c62355458f7">CVssWriter::SetWriterFailure</a>



<a href="https://msdn.microsoft.com/e8ff2491-014c-43c7-bdce-99ed3b408605">IVssWriterComponents</a>
 

 

