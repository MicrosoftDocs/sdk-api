---
UID: NF:vswriter.CVssWriter.OnAbort
title: CVssWriter::OnAbort
author: windows-sdk-content
description: The OnAbort method is called by a writer following an Abort event issued by VSS indicating that a shadow copy operation has terminated prematurely. The writer uses this method to clean up from its attempt to participate in that operation.
old-location: base\cvsswriter_onabort.htm
old-project: vss
ms.assetid: 56ba5f08-4803-4137-9edd-ce05bc19773b
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: CVssWriter interface [VSS],OnAbort method, CVssWriter.OnAbort, CVssWriter::OnAbort, OnAbort, OnAbort method [VSS], OnAbort method [VSS],CVssWriter interface, _win32_cvsswriter_onabort, base.cvsswriter_onabort, vswriter/CVssWriter::OnAbort
ms.prod: windows
ms.technology: windows-sdk
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
 - CVssWriter.OnAbort
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# CVssWriter::OnAbort


## -description


The 
<b>OnAbort</b> method is called by a writer following an <a href="vssgloss_a.htm">Abort</a> event issued by VSS indicating that a shadow copy operation has terminated prematurely. The writer uses this method to clean up from its attempt to participate in that operation.

<b>OnAbort</b> is a pure virtual method. It is not implemented by the 
<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a> base class, and must be implemented by derived classes.


## -parameters






## -returns



The implementation of this method should return <b>true</b> except in the case of a fatal error. If a fatal error occurs, the method must call the <a href="https://msdn.microsoft.com/9fef9d77-dc0d-4ba0-a317-5c62355458f7">CVssWriter::SetWriterFailure</a> method to provide a description of the failure before returning <b>false</b>. If a nonfatal error occurs, the method should still call <b>SetWriterFailure</b> but return <b>true</b>. If the error is caused by a transient problem, the method should specify VSS_E_WRITERERROR_RETRYABLE in the call to <b>SetWriterFailure</b>.

  In all cases when a failure occurs, the method should write an event to the event log to report the exact reason for the failure.




## -remarks



In this method, the writer should free all temporary system resources it created when preparing to participate with a VSS operation.

The writer will not receive further event notifications related to the VSS operation it was participating in after 
<b>CVssWriter::OnAbort</b> has been executed.

This method will not be called if the writer has called 
<a href="https://msdn.microsoft.com/d97d4246-882e-49c3-a214-d8d3887c1508">CVssWriter::OnPostSnapshot</a> (that is, received notification of the end of a shadow copy).

An Abort event is generated when:

<ul>
<li>A writer's <a href="vssgloss_f.htm">Freeze</a> and <a href="vssgloss_t.htm">Thaw</a> event handlers (<a href="https://msdn.microsoft.com/2aff5e87-4053-46a0-a7fb-7411e76166ba">CVssWriter::OnFreeze</a> and 
<a href="https://msdn.microsoft.com/36028e9f-f7a7-41f1-a570-48f943e9ab83">CVssWriter::OnThaw</a>) return <b>false</b>, or cannot complete in the time window specified in 
<a href="https://msdn.microsoft.com/a427ebbd-b7c4-46ba-ba16-dd601b1f956e">CVssWriter::Initialize</a>.</li>
<li>A requester explicitly generates an Abort event by calling 
<a href="https://msdn.microsoft.com/e854ab83-9a1a-4660-8a3e-37747b1b7d8c">IVssBackupComponents::AbortBackup</a>.</li>
<li>There is any failure of the provider or VSS during the creation of a shadow copy following the <a href="vssgloss_p.htm">PrepareForSnapshot</a> event.</li>
</ul>
Writers should never throw an exception from this method or any other <b>CVssWriter(Ex)::On<i>Xxx</i></b> callback method.

If this method calls the <a href="https://msdn.microsoft.com/bea5ba9c-538b-453f-ae6d-12b94b8edeb6">CVssWriterEx2::GetSessionId</a>, <a href="https://msdn.microsoft.com/9fef9d77-dc0d-4ba0-a317-5c62355458f7">CVssWriter::SetWriterFailure</a>, or <a href="https://msdn.microsoft.com/c049a016-6546-4e72-90e8-46be8c2f7764">CVssWriterEx2::SetWriterFailureEx</a> method, it must do so in  the same thread that called this method. For more information, see 
<a href="writers.htm">Writer Event Handling</a>.




## -see-also




<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a>



<a href="https://msdn.microsoft.com/2aff5e87-4053-46a0-a7fb-7411e76166ba">CVssWriter::OnFreeze</a>



<a href="https://msdn.microsoft.com/d97d4246-882e-49c3-a214-d8d3887c1508">CVssWriter::OnPostSnapshot</a>



<a href="https://msdn.microsoft.com/a077323e-d04c-4bf7-8aa6-5028fa1c6e6b">CVssWriter::OnPrepareSnapshot</a>



<a href="https://msdn.microsoft.com/36028e9f-f7a7-41f1-a570-48f943e9ab83">CVssWriter::OnThaw</a>



<a href="https://msdn.microsoft.com/9fef9d77-dc0d-4ba0-a317-5c62355458f7">CVssWriter::SetWriterFailure</a>
 

 

