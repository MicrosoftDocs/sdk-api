---
UID: NF:vswriter.CVssWriter.OnPostRestore
title: CVssWriter::OnPostRestore (vswriter.h)
description: The OnPostRestore method is called by a writer following a PostRestore event. It is used to perform operations considered necessary after files are restored to disk by a requester. These operations cannot, however, modify the Backup Components Document.
helpviewer_keywords: ["CVssWriter interface [VSS]","OnPostRestore method","CVssWriter.OnPostRestore","CVssWriter::OnPostRestore","OnPostRestore","OnPostRestore method [VSS]","OnPostRestore method [VSS]","CVssWriter interface","_win32_cvsswriter_onpostrestore","base.cvsswriter_onpostrestore","vswriter/CVssWriter::OnPostRestore"]
old-location: base\cvsswriter_onpostrestore.htm
tech.root: base
ms.assetid: ad07753c-1592-4fc8-9899-a73e798c158c
ms.date: 12/05/2018
ms.keywords: CVssWriter interface [VSS],OnPostRestore method, CVssWriter.OnPostRestore, CVssWriter::OnPostRestore, OnPostRestore, OnPostRestore method [VSS], OnPostRestore method [VSS],CVssWriter interface, _win32_cvsswriter_onpostrestore, base.cvsswriter_onpostrestore, vswriter/CVssWriter::OnPostRestore
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
 - CVssWriter::OnPostRestore
 - vswriter/CVssWriter::OnPostRestore
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
 - CVssWriter.OnPostRestore
---

# CVssWriter::OnPostRestore


## -description

The 
<b>OnPostRestore</b> method is called by a writer following a 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-postrestore">PostRestore</a> event. It is used to perform operations considered necessary after files are restored to disk by a requester. These operations cannot, however, modify the Backup Components Document.

<b>OnPostRestore</b> is a virtual method. It is implemented by the 
<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> base class, but can be overridden by derived classes.

## -parameters

### -param pComponent [in]

A pointer to an 
<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswritercomponents">IVssWriterComponents</a> object passed in by VSS to provide the method with access to the writer's component information. The value of this parameter may be <b>NULL</b> if the requester does not support components (if 
<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-arecomponentsselected">CVssWriter::AreComponentsSelected</a> returns <b>false</b>).

## -returns

As implemented by the base class, 
<b>OnPostRestore</b> always returns <b>true</b>.

Any other implementation of this method must return <b>true</b> except in the case of a fatal error.
      If a fatal error occurs, the method must call the <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure">CVssWriter::SetWriterFailure</a> method to provide a description of the failure before returning <b>false</b>. If a nonfatal error occurs, the method should still call <b>SetWriterFailure</b> but return <b>true</b>. If the error is caused by a transient problem, the method should specify VSS_E_WRITERERROR_RETRYABLE in the call to <b>SetWriterFailure</b>.

  In all cases when a failure occurs, the method should write an event to the event log to report the exact reason for the failure.

## -remarks

The default implementation of this method by the 
<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> base class returns <b>true</b> without performing any other operation.

If necessary, a writer should remove any temporary files and release any system resources that it needed for its participation in the restore.

Writers should never throw an exception from this method or any other <b>CVssWriter(Ex)::On<i>Xxx</i></b> callback method.

With the generation of a 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-postrestore">PostRestore</a> event, a requester's Backup Components Document becomes a read-only document. Therefore, attempts to modify the document through the interface (for instance, calling 
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-setrestoremetadata">IVssComponent::SetRestoreMetadata</a>) will fail in user implementations of 
<b>OnPostRestore</b>.

If this method calls the <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriterex2-getsessionid">CVssWriterEx2::GetSessionId</a>, <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure">CVssWriter::SetWriterFailure</a>, or <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriterex2-setwriterfailureex">CVssWriterEx2::SetWriterFailureEx</a> method, it must do so in  the same thread that called this method. For more information, see 
<a href="/windows/desktop/VSS/writers">Writer Event Handling</a>.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a>



<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswritercomponents">IVssWriterComponents</a>