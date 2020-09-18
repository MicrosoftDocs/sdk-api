---
UID: NF:vswriter.CVssWriter.OnPostSnapshot
title: CVssWriter::OnPostSnapshot (vswriter.h)
description: The OnPostSnapshot method is called by a writer following a PostSnapshot event.
helpviewer_keywords: ["CVssWriter class [VSS]","OnPostSnapshot method","CVssWriter.OnPostSnapshot","CVssWriter::OnPostSnapshot","OnPostSnapshot","OnPostSnapshot method [VSS]","OnPostSnapshot method [VSS]","CVssWriter class","_win32_cvsswriter_onpostsnapshot","base.cvsswriter_onpostsnapshot","vswriter/CVssWriter::OnPostSnapshot"]
old-location: base\cvsswriter_onpostsnapshot.htm
tech.root: base
ms.assetid: d97d4246-882e-49c3-a214-d8d3887c1508
ms.date: 12/05/2018
ms.keywords: CVssWriter class [VSS],OnPostSnapshot method, CVssWriter.OnPostSnapshot, CVssWriter::OnPostSnapshot, OnPostSnapshot, OnPostSnapshot method [VSS], OnPostSnapshot method [VSS],CVssWriter class, _win32_cvsswriter_onpostsnapshot, base.cvsswriter_onpostsnapshot, vswriter/CVssWriter::OnPostSnapshot
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
 - CVssWriter::OnPostSnapshot
 - vswriter/CVssWriter::OnPostSnapshot
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
 - CVssWriter.OnPostSnapshot
---

# CVssWriter::OnPostSnapshot


## -description

The <b>OnPostSnapshot</b> method is called by a 
    writer following a <a href="/windows/desktop/VSS/vssgloss-p">PostSnapshot</a> 
    event.

<b>OnPostSnapshot</b> is a virtual method. It is 
    implemented by the <a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> base class but can be 
    overridden by derived classes.

## -parameters

### -param pComponent [in]

A pointer to an <a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswritercomponents">IVssWriterComponents</a> object 
      passed in by VSS to provide the method with access to the writer's component information. The value of this 
      parameter may be NULL if the requester does not support components (if 
      <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-arecomponentsselected">CVssWriter::AreComponentsSelected</a> 
      returns <b>false</b>).

## -returns

As implemented by the base class, 
       <b>OnPostSnapshot</b> always returns <b>true</b>.

Any other implementation of this method must return <b>true</b> except in the case of a fatal error.
      If a fatal error occurs, the method must call the <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure">CVssWriter::SetWriterFailure</a> method to provide a description of the failure before returning <b>false</b>. If a nonfatal error occurs, the method should still call <b>SetWriterFailure</b> but return <b>true</b>. If the error is caused by a transient problem, the method should specify VSS_E_WRITERERROR_RETRYABLE in the call to <b>SetWriterFailure</b>.

  In all cases when a failure occurs, the method should write an event to the event log to report the exact reason for the failure.

## -remarks

The default implementation of this method by the 
    <a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> base class returns <b>true</b> without 
    performing any other operation.

<b>CVssWriter::OnPostSnapshot</b> is typically 
       used to process any final updates by the writer to the backup components metadata and clean up (such as 
       removing temporary files).

If an incremental or differential backup is being performed, the writer may call <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp">IVssComponent::GetPreviousBackupStamp</a> and <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-setbackupstamp">IVssComponent::SetBackupStamp</a>. For more information, see <a href="/windows/desktop/VSS/writer-role-in-backing-up-complex-stores">Writer Role in Backing Up Complex Stores</a>. Another method that can be called at this time is <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime">IVssComponent::AddDifferencedFilesByLastModifyTime</a>.

Most of the work needed to return the writer to normal operation (reversing the actions of 
       <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpreparesnapshot">CVssWriter::OnPrepareSnapshot</a> and 
       <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onfreeze">CVssWriter::OnFreeze</a>) is typically performed in 
       <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onthaw">CVssWriter::OnThaw</a>, not in 
       <b>OnPostSnapshot</b>.

Writers should never throw an exception from this method or any other <b>CVssWriter(Ex)::On<i>Xxx</i></b> callback method.

 If the shadow copy has the <b>VSS_VOLSNAP_ATTR_AUTORECOVER</b> flag set in the context, 
    the writer should perform any recovery required (for example, rolling back any incomplete transactions) so that 
    the component will be usable on a read-only copy for data mining (without adding load to the live server) or 
    restore purposes (for example, to restore selected items from a database).

To retrieve the volume name of the shadow copy of a volume, perform the following steps:

<ol>
<li>Call the <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-getcurrentvolumecount">CVssWriter::GetCurrentVolumeCount</a> method to query the number of volumes in the shadow copy set.</li>
<li>Call the <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-getcurrentvolumearray">CVssWriter::GetCurrentVolumeArray</a> method to enumerate the original names of the volumes in the shadow copy set.</li>
<li>Call the <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-getsnapshotdevicename">CVssWriter::GetSnapshotDeviceName</a> to retrieve the name of the shadow copy volume.</li>
</ol>
If this method calls the <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriterex2-getsessionid">CVssWriterEx2::GetSessionId</a>, <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure">CVssWriter::SetWriterFailure</a>, or <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriterex2-setwriterfailureex">CVssWriterEx2::SetWriterFailureEx</a> method, it must do so in  the same thread that called this method. For more information, see 
<a href="/windows/desktop/VSS/writers">Writer Event Handling</a>.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-getsnapshotdevicename">CVssWriter::GetSnapshotDeviceName</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onprerestore">CVssWriter::OnPreRestore</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpreparebackup">CVssWriter::OnPrepareBackup</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure">CVssWriter::SetWriterFailure</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onthaw">CvssWriter::OnThaw</a>



<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswritercomponents">IVssWriterComponents</a>