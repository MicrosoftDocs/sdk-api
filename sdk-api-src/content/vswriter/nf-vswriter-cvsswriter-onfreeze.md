---
UID: NF:vswriter.CVssWriter.OnFreeze
title: CVssWriter::OnFreeze (vswriter.h)
author: windows-sdk-content
description: The OnFreeze method is called by a writer on receipt of a Freeze event at the start of a shadow copy freeze. A writer uses this method to perform operations needed to participate in the freeze or to veto the freeze.
old-location: base\cvsswriter_onfreeze.htm
tech.root: VSS
ms.assetid: 2aff5e87-4053-46a0-a7fb-7411e76166ba
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CVssWriter interface [VSS],OnFreeze method, CVssWriter.OnFreeze, CVssWriter::OnFreeze, OnFreeze, OnFreeze method [VSS], OnFreeze method [VSS],CVssWriter interface, _win32_cvsswriter_onfreeze, base.cvsswriter_onfreeze, vswriter/CVssWriter::OnFreeze
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
 - CVssWriter.OnFreeze
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CVssWriter::OnFreeze


## -description


The 
<b>OnFreeze</b> method is called by a writer on receipt of a <a href="https://msdn.microsoft.com/en-us/library/Aa384656(v=VS.85).aspx">Freeze</a> event at the start of a shadow copy freeze. A writer uses this method to perform operations needed to participate in the freeze or to veto the freeze.

<b>OnFreeze</b> is a pure virtual method. It is not implemented by the 
<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a> base class, and must be implemented by derived classes.


## -parameters






## -returns



The implementation of this method must return <b>true</b> except in the case of a fatal error.
      If a fatal error occurs, the method must call the <a href="https://msdn.microsoft.com/9fef9d77-dc0d-4ba0-a317-5c62355458f7">CVssWriter::SetWriterFailure</a> method to provide a description of the failure before returning <b>false</b>. If a nonfatal error occurs, the method should still call  <b>SetWriterFailure</b> but return <b>true</b>. If the error is caused by a transient problem, the method should specify VSS_E_WRITERERROR_RETRYABLE in the call to <b>SetWriterFailure</b>.

  In all cases when a failure occurs, the method should write an event to the event log to report the exact reason for the failure.




## -remarks



In this method, the writer application should put itself into a well-defined state that is compatible with the VSS operation.
   

In this method, the writer should complete final preparations to support the creation of a shadow copy. Once the shadow copy is created, the writer will receive the <a href="https://msdn.microsoft.com/en-us/library/Aa384668(v=VS.85).aspx">Thaw</a> event and can continue normal operations.

By default, the time-out window between Freeze and Thaw events is 60 seconds. That is, if a Thaw event is not received with the time-out window, an Abort event will be generated. Writers can change the time-out window at initialization time by setting the <i>dwTimeoutFreeze</i> argument to 
<a href="https://msdn.microsoft.com/a427ebbd-b7c4-46ba-ba16-dd601b1f956e">CVssWriter::Initialize</a>.

How a writer prepares for a shadow copy is highly dependent on the application that hosts it. Some applications can afford to hold all writes and keep the data in an absolute consistent state for this period. Other applications, like many databases, cannot stop work during this period but can take actions, such as checkpointing their state, which may reduce the recovery time for a shadow copy created during this window.

If the writer cannot put itself into a well-defined state for the Freeze, the following happens:

<ol>
<li><b>OnFreeze</b> should return <b>false</b>, vetoing the shadow copy.</li>
<li>The writer calls 
<a href="https://msdn.microsoft.com/9fef9d77-dc0d-4ba0-a317-5c62355458f7">CVssWriter::SetWriterFailure</a> to provide a description of the failure.</li>
<li>An Abort event will be generated upon <b>OnFreeze</b> return of <b>false</b></li>
</ol>
Writers should never throw an exception from this method or any other <b>CVssWriter(Ex)::On<i>Xxx</i></b> callback method.

The time-out window for handling the Freeze event is typically relatively short as compared to that for handling the <a href="https://msdn.microsoft.com/en-us/library/Aa384664(v=VS.85).aspx">PrepareForSnapshot</a> event. Therefore, developers should avoid lengthy operations in this method. A typical use might be to suspend logging by the writer.

It is recommended that all time-consuming operations be handled by 
<a href="https://msdn.microsoft.com/a077323e-d04c-4bf7-8aa6-5028fa1c6e6b">CVssWriter::OnPrepareSnapshot</a>.

Either 
<a href="https://msdn.microsoft.com/36028e9f-f7a7-41f1-a570-48f943e9ab83">CVssWriter::OnThaw</a> or 
<a href="https://msdn.microsoft.com/56ba5f08-4803-4137-9edd-ce05bc19773b">CVssWriter::OnAbort</a> will be called after this method.

If this method calls the <a href="https://msdn.microsoft.com/bea5ba9c-538b-453f-ae6d-12b94b8edeb6">CVssWriterEx2::GetSessionId</a>, <a href="https://msdn.microsoft.com/9fef9d77-dc0d-4ba0-a317-5c62355458f7">CVssWriter::SetWriterFailure</a>, or <a href="https://msdn.microsoft.com/c049a016-6546-4e72-90e8-46be8c2f7764">CVssWriterEx2::SetWriterFailureEx</a> method, it must do so in  the same thread that called this method. For more information, see 
<a href="https://msdn.microsoft.com/en-us/library/Aa384993(v=VS.85).aspx">Writer Event Handling</a>.




## -see-also




<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a>



<a href="https://msdn.microsoft.com/56ba5f08-4803-4137-9edd-ce05bc19773b">CVssWriter::OnAbort</a>



<a href="https://msdn.microsoft.com/5f4a6168-4102-4790-81d6-d195a440471f">CVssWriter::OnPreRestore</a>



<a href="https://msdn.microsoft.com/4e88d92b-48f3-42f9-bf66-61337a745902">CVssWriter::OnPrepareBackup</a>



<a href="https://msdn.microsoft.com/a077323e-d04c-4bf7-8aa6-5028fa1c6e6b">CVssWriter::OnPrepareSnapshot</a>



<a href="https://msdn.microsoft.com/36028e9f-f7a7-41f1-a570-48f943e9ab83">CVssWriter::OnThaw</a>



<a href="https://msdn.microsoft.com/9fef9d77-dc0d-4ba0-a317-5c62355458f7">CVssWriter::SetWriterFailure</a>
 

 

