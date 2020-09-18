---
UID: NF:vswriter.CVssWriter.OnBackupComplete
title: CVssWriter::OnBackupComplete (vswriter.h)
description: The OnBackupComplete method is called by a writer following a BackupComplete event. It is used to perform operations considered necessary following a backup. These operations cannot, however, modify the Backup Components Document.
helpviewer_keywords: ["CVssWriter interface [VSS]","OnBackupComplete method","CVssWriter.OnBackupComplete","CVssWriter::OnBackupComplete","OnBackupComplete","OnBackupComplete method [VSS]","OnBackupComplete method [VSS]","CVssWriter interface","_win32_cvsswriter_onbackupcomplete","base.cvsswriter_onbackupcomplete","vswriter/CVssWriter::OnBackupComplete"]
old-location: base\cvsswriter_onbackupcomplete.htm
tech.root: base
ms.assetid: 77d0621d-81bd-4d53-8e5d-f5d3bfd86013
ms.date: 12/05/2018
ms.keywords: CVssWriter interface [VSS],OnBackupComplete method, CVssWriter.OnBackupComplete, CVssWriter::OnBackupComplete, OnBackupComplete, OnBackupComplete method [VSS], OnBackupComplete method [VSS],CVssWriter interface, _win32_cvsswriter_onbackupcomplete, base.cvsswriter_onbackupcomplete, vswriter/CVssWriter::OnBackupComplete
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
 - CVssWriter::OnBackupComplete
 - vswriter/CVssWriter::OnBackupComplete
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
 - CVssWriter.OnBackupComplete
---

# CVssWriter::OnBackupComplete


## -description

The <b>OnBackupComplete</b> method is called by a 
    writer following a <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-backupcomplete">BackupComplete</a> event. 
    It is used to perform operations considered necessary following a backup. These operations cannot, however, modify 
    the Backup Components Document.
   

<b>OnBackupComplete</b> is a virtual method. It is
   implemented by the <a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> base class, but can be overridden 
   by derived classes.

## -parameters

### -param pComponent [in]

A pointer to an <a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswritercomponents">IVssWriterComponents</a> object 
      passed in by VSS to provide the method with access to the writer's component information. The value of this 
      parameter may be <b>NULL</b> if the requester does not support components (if 
      <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-arecomponentsselected">CVssWriter::AreComponentsSelected</a> returns
      <b>false</b>).

## -returns

As implemented by the base class, 
       <b>OnBackupComplete</b> always returns <b>true</b>.
      

Any other implementation of this method should return <b>true</b> except in the case of a fatal error.
      If a fatal error occurs, the method must call the <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure">CVssWriter::SetWriterFailure</a> method to provide a description of the failure before returning <b>false</b>. If a nonfatal error occurs, the method should still call <b>SetWriterFailure</b> but return <b>true</b>. If the error is caused by a transient problem, the method should specify VSS_E_WRITERERROR_RETRYABLE in the call to <b>SetWriterFailure</b>.

  In all cases when a failure occurs, the method should write an event to the event log to report the exact reason for the failure.

## -remarks

The default implementation of this method by 
    <a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> base class returns <b>true</b> without 
    performing any other operation.
   

If special operations are to be performed by the writer at the end of a backup, 
    the default implementation can be overridden.
   

With the generation of a 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-backupcomplete">BackupComplete</a> event, a 
    requester's Backup Components Document becomes a read-only document. Therefore, attempts to modify the 
    document through the interface (for instance, calling 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-setbackupmetadata">IVssComponent::SetBackupMetadata</a>) will 
    fail in user implementations of 
    <b>OnBackupComplete</b>.
   

A successful backup application will generate a 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-backupcomplete">BackupComplete</a> event when all data 
    has been saved to backup media.
   

However, there is no guarantee of the writer receiving a 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-backupcomplete">BackupComplete</a> event notification,
    because these require the backup application to either successfully complete the backup or fail gracefully.
   

A <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-backupcomplete">BackupComplete</a> event could fail to 
    be generated should the backup application be terminated by the system or manually prior to the completion of the
    backup (for instance, if the backup operation hung and had to be shut down).
   

A writer should maintain state information so that it can track whether a 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-backupcomplete">BackupComplete</a> event was sent for a
    given shadow copy set.
   

This information can be used by a writer's 
    <a href="/windows/desktop/VSS/vssgloss-b">BackupShutdown</a> event handler 
    (<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onbackupshutdown">CVssWriter::OnBackupShutdown</a>), 
    which will be called when a backup application actually terminates and its 
    <a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a> is released, to perform 
    cleanup operations should there be no call to 
    <b>OnBackupComplete</b>.
   

Writers should never throw an exception from this method or any other <b>CVssWriter(Ex)::On<i>Xxx</i></b> callback method.

If this method calls the <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriterex2-getsessionid">CVssWriterEx2::GetSessionId</a>, <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure">CVssWriter::SetWriterFailure</a>, or <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriterex2-setwriterfailureex">CVssWriterEx2::SetWriterFailureEx</a> method, it must do so in  the same thread that called this method. For more information, see 
<a href="/windows/desktop/VSS/writers">Writer Event Handling</a>.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure">CVssWriter::SetWriterFailure</a>



<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswritercomponents">IVssWriterComponents</a>