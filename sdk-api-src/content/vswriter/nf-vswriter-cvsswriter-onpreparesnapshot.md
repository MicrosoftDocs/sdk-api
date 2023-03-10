---
UID: NF:vswriter.CVssWriter.OnPrepareSnapshot
title: CVssWriter::OnPrepareSnapshot (vswriter.h)
description: The OnPrepareSnapshot method is called by a writer to handle a PrepareForSnapshot event. It is used to perform operations needed to prepare a writer to participate in the shadow copy or to veto a shadow copy.
helpviewer_keywords: ["CVssWriter interface [VSS]","OnPrepareSnapshot method","CVssWriter.OnPrepareSnapshot","CVssWriter::OnPrepareSnapshot","OnPrepareSnapshot","OnPrepareSnapshot method [VSS]","OnPrepareSnapshot method [VSS]","CVssWriter interface","_win32_cvsswriter_onpreparesnapshot","base.cvsswriter_onpreparesnapshot","vswriter/CVssWriter::OnPrepareSnapshot"]
old-location: base\cvsswriter_onpreparesnapshot.htm
tech.root: base
ms.assetid: a077323e-d04c-4bf7-8aa6-5028fa1c6e6b
ms.date: 12/05/2018
ms.keywords: CVssWriter interface [VSS],OnPrepareSnapshot method, CVssWriter.OnPrepareSnapshot, CVssWriter::OnPrepareSnapshot, OnPrepareSnapshot, OnPrepareSnapshot method [VSS], OnPrepareSnapshot method [VSS],CVssWriter interface, _win32_cvsswriter_onpreparesnapshot, base.cvsswriter_onpreparesnapshot, vswriter/CVssWriter::OnPrepareSnapshot
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
 - CVssWriter::OnPrepareSnapshot
 - vswriter/CVssWriter::OnPrepareSnapshot
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
 - CVssWriter.OnPrepareSnapshot
---

# CVssWriter::OnPrepareSnapshot


## -description

The 
<b>OnPrepareSnapshot</b> method is called by a writer to handle a <a href="/windows/desktop/VSS/vssgloss-p">PrepareForSnapshot</a> event. It is used to perform operations needed to prepare a writer to participate in the shadow copy or to veto a shadow copy.

<b>OnPrepareSnapshot</b> is a pure virtual method. It is not implemented by the 
<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> base class, and must be implemented by derived classes.



## -returns

The implementation of this method must return <b>true</b> except in the case of a fatal error.
      If a fatal error occurs, the method must call the <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure">CVssWriter::SetWriterFailure</a> method to provide a description of the failure before returning <b>false</b>. If a nonfatal error occurs, the method should still call  <b>SetWriterFailure</b> but return <b>true</b>. If the error is caused by a transient problem, the method should specify VSS_E_WRITERERROR_RETRYABLE in the call to <b>SetWriterFailure</b>.

  In all cases when a failure occurs, the method should write an event to the event log to report the exact reason for the failure.

## -remarks

The 
<b>OnPrepareSnapshot</b> method performs operations that are required prior to any shadow copy freeze.

The time-out window for handling a <a href="/windows/desktop/VSS/vssgloss-p">PrepareForSnapshot</a> event is typically longer than that for handling a <a href="/windows/desktop/VSS/vssgloss-f">Freeze</a> event. Therefore, developers can use 
<b>OnPrepareSnapshot</b> to handle more time-consuming operations. A typical use might be for the writer to explicitly checkpoint its data.

Writers should never throw an exception from this method or any other <b>CVssWriter(Ex)::On<i>Xxx</i></b> callback method.

If this method calls the <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriterex2-getsessionid">CVssWriterEx2::GetSessionId</a>, <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure">CVssWriter::SetWriterFailure</a>, or <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriterex2-setwriterfailureex">CVssWriterEx2::SetWriterFailureEx</a> method, it must do so in  the same thread that called this method. For more information, see 
<a href="/windows/desktop/VSS/writers">Writer Event Handling</a>.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onabort">CVssWriter::OnAbort</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onfreeze">CVssWriter::OnFreeze</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onthaw">CVssWriter::OnThaw</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure">CVssWriter::SetWriterFailure</a>
