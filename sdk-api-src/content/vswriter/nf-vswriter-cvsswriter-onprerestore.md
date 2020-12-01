---
UID: NF:vswriter.CVssWriter.OnPreRestore
title: CVssWriter::OnPreRestore (vswriter.h)
description: The OnPreRestore method is called by a writer following a PreRestore event.
helpviewer_keywords: ["CVssWriter interface [VSS]","OnPreRestore method","CVssWriter.OnPreRestore","CVssWriter::OnPreRestore","OnPreRestore","OnPreRestore method [VSS]","OnPreRestore method [VSS]","CVssWriter interface","_win32_cvsswriter_onprerestore","base.cvsswriter_onprerestore","vswriter/CVssWriter::OnPreRestore"]
old-location: base\cvsswriter_onprerestore.htm
tech.root: base
ms.assetid: 5f4a6168-4102-4790-81d6-d195a440471f
ms.date: 12/05/2018
ms.keywords: CVssWriter interface [VSS],OnPreRestore method, CVssWriter.OnPreRestore, CVssWriter::OnPreRestore, OnPreRestore, OnPreRestore method [VSS], OnPreRestore method [VSS],CVssWriter interface, _win32_cvsswriter_onprerestore, base.cvsswriter_onprerestore, vswriter/CVssWriter::OnPreRestore
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
 - CVssWriter::OnPreRestore
 - vswriter/CVssWriter::OnPreRestore
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
 - CVssWriter.OnPreRestore
---

# CVssWriter::OnPreRestore


## -description

The 
<b>OnPreRestore</b> method is called by a writer following a 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prerestore">PreRestore</a> event. This method is used to put the writer in a state to support the restore—for instance, taking database services offline—and to make modifications in the Backup Components Document of the requester that is restoring files (such as setting the restore target to override the original restore method).

<b>OnPreRestore</b> is a virtual method. It is implemented by the 
<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> base class, but can be overridden by derived classes.

## -parameters

### -param pComponent [in]

Pointer to an instantiation of an 
<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswritercomponents">IVssWriterComponents</a> object containing those components associated with the current writer in the requester's Backup Components Document.

## -returns

As implemented by the base class, 
<b>OnPreRestore</b> always returns <b>true</b>.

Any other implementation of this method must return <b>true</b> except in the case of a fatal error.
      If a fatal error occurs, the method must call the <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure">CVssWriter::SetWriterFailure</a> method to provide a description of the failure before returning <b>false</b>. If a nonfatal error occurs, the method should still call <b>SetWriterFailure</b> but return <b>true</b>. If the error is caused by a transient problem, the method should specify VSS_E_WRITERERROR_RETRYABLE in the call to <b>SetWriterFailure</b>.

  In all cases when a failure occurs, the method should write an event to the event log to report the exact reason for the failure.

## -remarks

The 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prerestore">PreRestore</a> event occurs before backed-up data is actually being restored. This is an opportunity for the writer to determine what is being restored.

The default implementation of this method by the 
<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> base class returns <b>true</b> without performing any other operation.

This method enables the writer to determine what is being restored, to retrieve stored private metadata in the stored Backup Components Document, and to update that data.

Writers should never throw an exception from this method or any other <b>CVssWriter(Ex)::On<i>Xxx</i></b> callback method.

If this method calls the <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriterex2-getsessionid">CVssWriterEx2::GetSessionId</a>, <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure">CVssWriter::SetWriterFailure</a>, or <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriterex2-setwriterfailureex">CVssWriterEx2::SetWriterFailureEx</a> method, it must do so in  the same thread that called this method. For more information, see 
<a href="/windows/desktop/VSS/writers">Writer Event Handling</a>.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostsnapshot">CVssWriter::OnPostSnapshot</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpreparebackup">CVssWriter::OnPrepareBackup</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure">CVssWriter::SetWriterFailure</a>



<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswritercomponents">IVssWriterComponents</a>