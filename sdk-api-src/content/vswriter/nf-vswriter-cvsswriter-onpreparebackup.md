---
UID: NF:vswriter.CVssWriter.OnPrepareBackup
title: CVssWriter::OnPrepareBackup (vswriter.h)
description: The OnPrepareBackup method is called by a writer following a PrepareForBackup event. This method is used to configure a writer's state and its components in preparation for a backup operation.
helpviewer_keywords: ["CVssWriter interface [VSS]","OnPrepareBackup method","CVssWriter.OnPrepareBackup","CVssWriter::OnPrepareBackup","OnPrepareBackup","OnPrepareBackup method [VSS]","OnPrepareBackup method [VSS]","CVssWriter interface","_win32_cvsswriter_onpreparebackup","base.cvsswriter_onpreparebackup","vswriter/CVssWriter::OnPrepareBackup"]
old-location: base\cvsswriter_onpreparebackup.htm
tech.root: base
ms.assetid: 4e88d92b-48f3-42f9-bf66-61337a745902
ms.date: 12/05/2018
ms.keywords: CVssWriter interface [VSS],OnPrepareBackup method, CVssWriter.OnPrepareBackup, CVssWriter::OnPrepareBackup, OnPrepareBackup, OnPrepareBackup method [VSS], OnPrepareBackup method [VSS],CVssWriter interface, _win32_cvsswriter_onpreparebackup, base.cvsswriter_onpreparebackup, vswriter/CVssWriter::OnPrepareBackup
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
 - CVssWriter::OnPrepareBackup
 - vswriter/CVssWriter::OnPrepareBackup
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
 - CVssWriter.OnPrepareBackup
---

# CVssWriter::OnPrepareBackup


## -description

The 
<b>OnPrepareBackup</b> method is called by a writer following a 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup">PrepareForBackup</a> event. This method is used to configure a writer's state and its components in preparation for a backup operation.

<b>OnPrepareBackup</b> is a virtual method. It is implemented by the 
<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> base class, but can be overridden by derived classes.

## -parameters

### -param pComponent [in]

Pointer to an instantiation of an 
<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswritercomponents">IVssWriterComponents</a> object containing the contents of the Writer Metadata Document. The value of this parameter may be <b>NULL</b> if the requester does not support components (if 
<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-arecomponentsselected">CVssWriter::AreComponentsSelected</a> returns <b>false</b>).

## -returns

As implemented by the base class, 
<b>OnPrepareBackup</b> always returns <b>true</b>.

Any other implementation of this method must return <b>true</b> except in the case of a fatal error.
      If a fatal error occurs, the method must call the <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure">CVssWriter::SetWriterFailure</a> method to provide a description of the failure before returning <b>false</b>. If a nonfatal error occurs, the method should still call <b>SetWriterFailure</b> but return <b>true</b>. If the error is caused by a transient problem, the method should specify VSS_E_WRITERERROR_RETRYABLE in the call to <b>SetWriterFailure</b>.

  In all cases when a failure occurs, the method should write an event to the event log to report the exact reason for the failure.

## -remarks

The default implementation of this method by the 
<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> base class returns <b>true</b> without performing any other operation.

<b>OnPrepareBackup</b> provides a writer an opportunity to more finely select what will be backed up.

Handling the <a href="/windows/desktop/VSS/vssgloss-p">PrepareForBackup</a> event is the last opportunity for a writer to get access to metadata contained in the Backup Components Document prior to the shadow copy's creation.

Therefore, 
<b>OnPrepareBackup</b> provides an opportunity for the writer to make any final additions or updates to stored component information (using the 
<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a> interface). In particular, writer-specific metadata can be updated by 
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-setbackupmetadata">IVssComponent::SetBackupMetadata</a> or 
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-setrestoremetadata">IVssComponent::SetRestoreMetadata</a>.

In addition, while handling the <a href="/windows/desktop/VSS/vssgloss-p">PrepareForSnapshot</a> event provides another opportunity in the life cycle of a VSS backup operation to perform time-consuming operations (such as synchronizing data across multiple sites), 
<b>OnPrepareBackup</b> provides a chance for the writer to start such an operation asynchronously. Tasks like these must be completed prior to the return of 
<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpreparesnapshot">CVssWriter::OnPrepareSnapshot</a>.

Writers should never throw an exception from this method or any other <b>CVssWriter(Ex)::On<i>Xxx</i></b> callback method.

A requester generates a 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup">PrepareForBackup</a> event, triggering a call to 
<b>OnPrepareBackup</b>, by calling 
<b>IVssBackupComponents::PrepareForBackup</b>.

If this method calls the <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriterex2-getsessionid">CVssWriterEx2::GetSessionId</a>, <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure">CVssWriter::SetWriterFailure</a>, or <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriterex2-setwriterfailureex">CVssWriterEx2::SetWriterFailureEx</a> method, it must do so in  the same thread that called this method. For more information, see 
<a href="/windows/desktop/VSS/writers">Writer Event Handling</a>.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostsnapshot">CVssWriter::OnPostSnapshot</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onprerestore">CVssWriter::OnPreRestore</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure">CVssWriter::SetWriterFailure</a>



<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswritercomponents">IVssWriterComponents</a>