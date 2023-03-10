---
UID: NF:vswriter.CVssWriter.OnAbort
title: CVssWriter::OnAbort (vswriter.h)
description: The OnAbort method is called by a writer following an Abort event issued by VSS indicating that a shadow copy operation has terminated prematurely. The writer uses this method to clean up from its attempt to participate in that operation.
helpviewer_keywords: ["CVssWriter interface [VSS]","OnAbort method","CVssWriter.OnAbort","CVssWriter::OnAbort","OnAbort","OnAbort method [VSS]","OnAbort method [VSS]","CVssWriter interface","_win32_cvsswriter_onabort","base.cvsswriter_onabort","vswriter/CVssWriter::OnAbort"]
old-location: base\cvsswriter_onabort.htm
tech.root: base
ms.assetid: 56ba5f08-4803-4137-9edd-ce05bc19773b
ms.date: 12/05/2018
ms.keywords: CVssWriter interface [VSS],OnAbort method, CVssWriter.OnAbort, CVssWriter::OnAbort, OnAbort, OnAbort method [VSS], OnAbort method [VSS],CVssWriter interface, _win32_cvsswriter_onabort, base.cvsswriter_onabort, vswriter/CVssWriter::OnAbort
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
 - CVssWriter::OnAbort
 - vswriter/CVssWriter::OnAbort
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
 - CVssWriter.OnAbort
---

# CVssWriter::OnAbort


## -description

The 
<b>OnAbort</b> method is called by a writer following an <a href="/windows/desktop/VSS/vssgloss-a">Abort</a> event issued by VSS indicating that a shadow copy operation has terminated prematurely. The writer uses this method to clean up from its attempt to participate in that operation.

<b>OnAbort</b> is a pure virtual method. It is not implemented by the 
<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> base class, and must be implemented by derived classes.



## -returns

The implementation of this method should return <b>true</b> except in the case of a fatal error. If a fatal error occurs, the method must call the <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure">CVssWriter::SetWriterFailure</a> method to provide a description of the failure before returning <b>false</b>. If a nonfatal error occurs, the method should still call <b>SetWriterFailure</b> but return <b>true</b>. If the error is caused by a transient problem, the method should specify VSS_E_WRITERERROR_RETRYABLE in the call to <b>SetWriterFailure</b>.

  In all cases when a failure occurs, the method should write an event to the event log to report the exact reason for the failure.

## -remarks

In this method, the writer should free all temporary system resources it created when preparing to participate with a VSS operation.

The writer will not receive further event notifications related to the VSS operation it was participating in after 
<b>CVssWriter::OnAbort</b> has been executed.

This method will not be called if the writer has called 
<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostsnapshot">CVssWriter::OnPostSnapshot</a> (that is, received notification of the end of a shadow copy).

An Abort event is generated when:

<ul>
<li>A writer's <a href="/windows/desktop/VSS/vssgloss-f">Freeze</a> and <a href="/windows/desktop/VSS/vssgloss-t">Thaw</a> event handlers (<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onfreeze">CVssWriter::OnFreeze</a> and 
<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onthaw">CVssWriter::OnThaw</a>) return <b>false</b>, or cannot complete in the time window specified in 
<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-initialize">CVssWriter::Initialize</a>.</li>
<li>A requester explicitly generates an Abort event by calling 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-abortbackup">IVssBackupComponents::AbortBackup</a>.</li>
<li>There is any failure of the provider or VSS during the creation of a shadow copy following the <a href="/windows/desktop/VSS/vssgloss-p">PrepareForSnapshot</a> event.</li>
</ul>
Writers should never throw an exception from this method or any other <b>CVssWriter(Ex)::On<i>Xxx</i></b> callback method.

If this method calls the <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriterex2-getsessionid">CVssWriterEx2::GetSessionId</a>, <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure">CVssWriter::SetWriterFailure</a>, or <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriterex2-setwriterfailureex">CVssWriterEx2::SetWriterFailureEx</a> method, it must do so in  the same thread that called this method. For more information, see 
<a href="/windows/desktop/VSS/writers">Writer Event Handling</a>.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onfreeze">CVssWriter::OnFreeze</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostsnapshot">CVssWriter::OnPostSnapshot</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpreparesnapshot">CVssWriter::OnPrepareSnapshot</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onthaw">CVssWriter::OnThaw</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure">CVssWriter::SetWriterFailure</a>
