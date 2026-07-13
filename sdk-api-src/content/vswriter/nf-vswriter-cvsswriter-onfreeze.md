---
UID: NF:vswriter.CVssWriter.OnFreeze
title: CVssWriter::OnFreeze (vswriter.h)
description: The OnFreeze method is called by a writer on receipt of a Freeze event at the start of a shadow copy freeze. A writer uses this method to perform operations needed to participate in the freeze or to veto the freeze.
helpviewer_keywords: ["CVssWriter interface [VSS]","OnFreeze method","CVssWriter.OnFreeze","CVssWriter::OnFreeze","OnFreeze","OnFreeze method [VSS]","OnFreeze method [VSS]","CVssWriter interface","_win32_cvsswriter_onfreeze","base.cvsswriter_onfreeze","vswriter/CVssWriter::OnFreeze"]
old-location: base\cvsswriter_onfreeze.htm
tech.root: base
ms.assetid: 2aff5e87-4053-46a0-a7fb-7411e76166ba
ms.date: 12/05/2018
ms.keywords: CVssWriter interface [VSS],OnFreeze method, CVssWriter.OnFreeze, CVssWriter::OnFreeze, OnFreeze, OnFreeze method [VSS], OnFreeze method [VSS],CVssWriter interface, _win32_cvsswriter_onfreeze, base.cvsswriter_onfreeze, vswriter/CVssWriter::OnFreeze
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CVssWriter::OnFreeze
 - vswriter/CVssWriter::OnFreeze
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
 - CVssWriter.OnFreeze
---

# CVssWriter::OnFreeze


## -description

The 
<b>OnFreeze</b> method is called by a writer on receipt of a <a href="/windows/desktop/VSS/vssgloss-f">Freeze</a> event at the start of a shadow copy freeze. A writer uses this method to perform operations needed to participate in the freeze or to veto the freeze.

<b>OnFreeze</b> is a pure virtual method. It is not implemented by the 
<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> base class, and must be implemented by derived classes.



## -returns

The implementation of this method must return <b>true</b> except in the case of a fatal error.
      If a fatal error occurs, the method must call the <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure">CVssWriter::SetWriterFailure</a> method to provide a description of the failure before returning <b>false</b>. If a nonfatal error occurs, the method should still call  <b>SetWriterFailure</b> but return <b>true</b>. If the error is caused by a transient problem, the method should specify VSS_E_WRITERERROR_RETRYABLE in the call to <b>SetWriterFailure</b>.

  In all cases when a failure occurs, the method should write an event to the event log to report the exact reason for the failure.

## -remarks

In this method, the writer application should put itself into a well-defined state that is compatible with the VSS operation.
   

In this method, the writer should complete final preparations to support the creation of a shadow copy. Once the shadow copy is created, the writer will receive the <a href="/windows/desktop/VSS/vssgloss-t">Thaw</a> event and can continue normal operations.

By default, the time-out window between Freeze and Thaw events is 60 seconds. That is, if a Thaw event is not received with the time-out window, an Abort event will be generated. Writers can change the time-out window at initialization time by setting the <i>dwTimeoutFreeze</i> argument to 
<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-initialize">CVssWriter::Initialize</a>.

How a writer prepares for a shadow copy is highly dependent on the application that hosts it. Some applications can afford to hold all writes and keep the data in an absolute consistent state for this period. Other applications, like many databases, cannot stop work during this period but can take actions, such as checkpointing their state, which may reduce the recovery time for a shadow copy created during this window.

If the writer cannot put itself into a well-defined state for the Freeze, the following happens:

<ol>
<li><b>OnFreeze</b> should return <b>false</b>, vetoing the shadow copy.</li>
<li>The writer calls 
<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure">CVssWriter::SetWriterFailure</a> to provide a description of the failure.</li>
<li>An Abort event will be generated upon <b>OnFreeze</b> return of <b>false</b></li>
</ol>
Writers should never throw an exception from this method or any other <b>CVssWriter(Ex)::On<i>Xxx</i></b> callback method.

The time-out window for handling the Freeze event is typically relatively short as compared to that for handling the <a href="/windows/desktop/VSS/vssgloss-p">PrepareForSnapshot</a> event. Therefore, developers should avoid lengthy operations in this method. A typical use might be to suspend logging by the writer.

It is recommended that all time-consuming operations be handled by 
<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpreparesnapshot">CVssWriter::OnPrepareSnapshot</a>.

Either 
<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onthaw">CVssWriter::OnThaw</a> or 
<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onabort">CVssWriter::OnAbort</a> will be called after this method.

If this method calls the <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriterex2-getsessionid">CVssWriterEx2::GetSessionId</a>, <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure">CVssWriter::SetWriterFailure</a>, or <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriterex2-setwriterfailureex">CVssWriterEx2::SetWriterFailureEx</a> method, it must do so in  the same thread that called this method. For more information, see 
<a href="/windows/desktop/VSS/writers">Writer Event Handling</a>.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onabort">CVssWriter::OnAbort</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onprerestore">CVssWriter::OnPreRestore</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpreparebackup">CVssWriter::OnPrepareBackup</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpreparesnapshot">CVssWriter::OnPrepareSnapshot</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onthaw">CVssWriter::OnThaw</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure">CVssWriter::SetWriterFailure</a>
