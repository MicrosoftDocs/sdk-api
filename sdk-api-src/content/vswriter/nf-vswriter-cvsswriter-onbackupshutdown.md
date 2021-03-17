---
UID: NF:vswriter.CVssWriter.OnBackupShutdown
title: CVssWriter::OnBackupShutdown (vswriter.h)
description: The OnBackupShutdown method is called by a writer following a BackupShutdown event. It is used to perform operations considered necessary when a backup application shuts down, particularly in the case of a crash of the backup application.
helpviewer_keywords: ["CVssWriter interface [VSS]","OnBackupShutdown method","CVssWriter.OnBackupShutdown","CVssWriter::OnBackupShutdown","OnBackupShutdown","OnBackupShutdown method [VSS]","OnBackupShutdown method [VSS]","CVssWriter interface","_win32_cvsswriter_onbackupshutdown","base.cvsswriter_onbackupshutdown","vswriter/CVssWriter::OnBackupShutdown"]
old-location: base\cvsswriter_onbackupshutdown.htm
tech.root: base
ms.assetid: 4b6d5efe-703b-4245-81d8-e2fc7f650d4b
ms.date: 12/05/2018
ms.keywords: CVssWriter interface [VSS],OnBackupShutdown method, CVssWriter.OnBackupShutdown, CVssWriter::OnBackupShutdown, OnBackupShutdown, OnBackupShutdown method [VSS], OnBackupShutdown method [VSS],CVssWriter interface, _win32_cvsswriter_onbackupshutdown, base.cvsswriter_onbackupshutdown, vswriter/CVssWriter::OnBackupShutdown
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - CVssWriter::OnBackupShutdown
 - vswriter/CVssWriter::OnBackupShutdown
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
 - CVssWriter.OnBackupShutdown
---

# CVssWriter::OnBackupShutdown


## -description

The 
<b>OnBackupShutdown</b> method is called by a writer following a <a href="/windows/desktop/VSS/vssgloss-b">BackupShutdown</a> event. It is used to perform operations considered necessary when a backup application shuts down, particularly in the case of a crash of the backup application.

<b>OnBackupShutdown</b> is a virtual method. It is implemented by the 
<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> base class, but can be overridden by derived classes.

## -parameters

### -param SnapshotSetId [in]

Identifier for the shadow copy set involved in the backup operation.

## -returns

As implemented by the base class, 
<b>OnBackupShutdown</b> always returns <b>true</b>

Any other implementation of this method should return <b>true</b> except in the case of a fatal error.
      If a fatal error occurs, the method must call the <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure">CVssWriter::SetWriterFailure</a> method to provide a description of the failure before returning <b>false</b>. If a nonfatal error occurs, the method should still call <b>SetWriterFailure</b> but return <b>true</b>. If the error is caused by a transient problem, the method should specify VSS_E_WRITERERROR_RETRYABLE in the call to <b>SetWriterFailure</b>.

  In all cases when a failure occurs, the method should write an event to the event log to report the exact reason for the failure.

## -remarks

The default implementation of this method by the 
<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> base class returns <b>true</b> without performing any other operation.

If special operations are to be performed by the writer when a backup application shuts down, the default implementation can be overridden.

If no shadow copy has been successfully performed, the value of the shadow copy set identifier (<i>SnapshotSetId</i>) will be <b>NULL</b>.

A BackupShutdown event will be generated whenever a backup application actually terminates and its 
<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a> is released.

The 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-backupcomplete">BackupComplete</a> event requires the backup application to either successfully complete the backup or fail gracefully; this may not be the case if the backup application is terminated by the system or terminated manually prior to the completion of the backup (for instance, if the backup operation hung and had to be shut down).

Because of this, a BackupShutdown event is a more robust signal of the end of a backup application than the 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-backupcomplete">BackupComplete</a> event.

A writer should maintain state information so that it can track whether a 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-backupcomplete">BackupComplete</a> event was sent for a given shadow copy set.

Any writer-specific implementation of 
<b>OnBackupShutdown</b> should check whether a 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-backupcomplete">BackupComplete</a> event was handled. It should ensure that all necessary writer cleanup operations following a backup (successful or otherwise) are preformed.

Writers should never throw an exception from this method or any other <b>CVssWriter(Ex)::On<i>Xxx</i></b> callback method.

If this method calls the <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriterex2-getsessionid">CVssWriterEx2::GetSessionId</a>, <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure">CVssWriter::SetWriterFailure</a>, or <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriterex2-setwriterfailureex">CVssWriterEx2::SetWriterFailureEx</a> method, it must do so in  the same thread that called this method. For more information, see 
<a href="/windows/desktop/VSS/writers">Writer Event Handling</a>.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onbackupcomplete">CVssWriter::OnBackupComplete</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure">CVssWriter::SetWriterFailure</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-backupcomplete">IVssBackupComponents::BackupComplete</a>