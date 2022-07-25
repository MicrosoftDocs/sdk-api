---
UID: NF:vswriter.CVssWriter.OnThaw
title: CVssWriter::OnThaw (vswriter.h)
description: The OnThaw method is called by a writer following a Thaw event.
helpviewer_keywords: ["CVssWriter interface [VSS]","OnThaw method","CVssWriter.OnThaw","CVssWriter::OnThaw","OnThaw","OnThaw method [VSS]","OnThaw method [VSS]","CVssWriter interface","_win32_cvsswriter_onthaw","base.cvsswriter_onthaw","vswriter/CVssWriter::OnThaw"]
old-location: base\cvsswriter_onthaw.htm
tech.root: base
ms.assetid: 36028e9f-f7a7-41f1-a570-48f943e9ab83
ms.date: 12/05/2018
ms.keywords: CVssWriter interface [VSS],OnThaw method, CVssWriter.OnThaw, CVssWriter::OnThaw, OnThaw, OnThaw method [VSS], OnThaw method [VSS],CVssWriter interface, _win32_cvsswriter_onthaw, base.cvsswriter_onthaw, vswriter/CVssWriter::OnThaw
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
 - CVssWriter::OnThaw
 - vswriter/CVssWriter::OnThaw
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
 - CVssWriter.OnThaw
---

# CVssWriter::OnThaw


## -description

The 
<b>OnThaw</b> method is called by a writer following a <a href="/windows/desktop/VSS/vssgloss-t">Thaw</a> event.

<b>OnThaw</b> is a pure virtual method. It is not implemented by the 
<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> base class, and must be implemented by derived classes.



## -returns

The implementation of this method must return <b>true</b> except in the case of a fatal error.
      If a fatal error occurs, the method must call the <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure">CVssWriter::SetWriterFailure</a> method to provide a description of the failure before returning <b>false</b>. If a nonfatal error occurs, the method should still call <b>SetWriterFailure</b> but return <b>true</b>. If the error is caused by a transient problem, the method should specify VSS_E_WRITERERROR_RETRYABLE in the call to <b>SetWriterFailure</b>.

  In all cases when a failure occurs, the method should write an event to the event log to report the exact reason for the failure.

## -remarks

This method is called at the end of a shadow copy freeze when writers can begin to modify data on disk again.

<b>OnThaw</b> is used to return the writer to normal operation, typically reversing actions taken during 
<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpreparesnapshot">CVssWriter::OnPrepareSnapshot</a> and 
<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onfreeze">CVssWriter::OnFreeze</a>.

Final updates by the writer to the backup components metadata and cleanup (such as removing temporary files) are typically reserved for 
<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostsnapshot">CVssWriter::OnPostSnapshot</a>.

Writers should never throw an exception from this method or any other <b>CVssWriter(Ex)::On<i>Xxx</i></b> callback method.

If this method calls the <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriterex2-getsessionid">CVssWriterEx2::GetSessionId</a>, <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure">CVssWriter::SetWriterFailure</a>, or <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriterex2-setwriterfailureex">CVssWriterEx2::SetWriterFailureEx</a> method, it must do so in  the same thread that called this method. For more information, see 
<a href="/windows/desktop/VSS/writers">Writer Event Handling</a>.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onabort">CVssWriter::OnAbort</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onfreeze">CVssWriter::OnFreeze</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostsnapshot">CVssWriter::OnPostSnapshot</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpreparesnapshot">CVssWriter::OnPrepareSnapshot</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure">CVssWriter::SetWriterFailure</a>
