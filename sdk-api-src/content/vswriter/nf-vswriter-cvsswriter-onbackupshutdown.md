---
UID: NF:vswriter.CVssWriter.OnBackupShutdown
title: CVssWriter::OnBackupShutdown
author: windows-sdk-content
description: The OnBackupShutdown method is called by a writer following a BackupShutdown event. It is used to perform operations considered necessary when a backup application shuts down, particularly in the case of a crash of the backup application.
old-location: base\cvsswriter_onbackupshutdown.htm
old-project: VSS
ms.assetid: 4b6d5efe-703b-4245-81d8-e2fc7f650d4b
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: CVssWriter interface [VSS],OnBackupShutdown method, CVssWriter.OnBackupShutdown, CVssWriter::OnBackupShutdown, OnBackupShutdown, OnBackupShutdown method [VSS], OnBackupShutdown method [VSS],CVssWriter interface, _win32_cvsswriter_onbackupshutdown, base.cvsswriter_onbackupshutdown, vswriter/CVssWriter::OnBackupShutdown
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: VSS_WRITERRESTORE_ENUM
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
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# CVssWriter::OnBackupShutdown


## -description


The 
<b>OnBackupShutdown</b> method is called by a writer following a <a href="https://docs.microsoft.com/windows/desktop//VSS/vssgloss-b">BackupShutdown</a> event. It is used to perform operations considered necessary when a backup application shuts down, particularly in the case of a crash of the backup application.

<b>OnBackupShutdown</b> is a virtual method. It is implemented by the 
<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a> base class, but can be overridden by derived classes.


## -parameters




### -param SnapshotSetId [in]

Identifier for the shadow copy set involved in the backup operation.


## -returns



As implemented by the base class, 
<b>OnBackupShutdown</b> always returns <b>true</b>

Any other implementation of this method should return <b>true</b> except in the case of a fatal error.
      If a fatal error occurs, the method must call the <a href="https://msdn.microsoft.com/9fef9d77-dc0d-4ba0-a317-5c62355458f7">CVssWriter::SetWriterFailure</a> method to provide a description of the failure before returning <b>false</b>. If a nonfatal error occurs, the method should still call <b>SetWriterFailure</b> but return <b>true</b>. If the error is caused by a transient problem, the method should specify VSS_E_WRITERERROR_RETRYABLE in the call to <b>SetWriterFailure</b>.

  In all cases when a failure occurs, the method should write an event to the event log to report the exact reason for the failure.




## -remarks



The default implementation of this method by the 
<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a> base class returns <b>true</b> without performing any other operation.

If special operations are to be performed by the writer when a backup application shuts down, the default implementation can be overridden.

If no shadow copy has been successfully performed, the value of the shadow copy set identifier (<i>SnapshotSetId</i>) will be <b>NULL</b>.

A BackupShutdown event will be generated whenever a backup application actually terminates and its 
<a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a> is released.

The 
<a href="https://msdn.microsoft.com/ee49d4b1-f3f4-4c85-a3a2-f4452d066f21">BackupComplete</a> event requires the backup application to either successfully complete the backup or fail gracefully; this may not be the case if the backup application is terminated by the system or terminated manually prior to the completion of the backup (for instance, if the backup operation hung and had to be shut down).

Because of this, a BackupShutdown event is a more robust signal of the end of a backup application than the 
<a href="https://msdn.microsoft.com/ee49d4b1-f3f4-4c85-a3a2-f4452d066f21">BackupComplete</a> event.

A writer should maintain state information so that it can track whether a 
<a href="https://msdn.microsoft.com/ee49d4b1-f3f4-4c85-a3a2-f4452d066f21">BackupComplete</a> event was sent for a given shadow copy set.

Any writer-specific implementation of 
<b>OnBackupShutdown</b> should check whether a 
<a href="https://msdn.microsoft.com/ee49d4b1-f3f4-4c85-a3a2-f4452d066f21">BackupComplete</a> event was handled. It should ensure that all necessary writer cleanup operations following a backup (successful or otherwise) are preformed.

Writers should never throw an exception from this method or any other <b>CVssWriter(Ex)::On<i>Xxx</i></b> callback method.

If this method calls the <a href="https://msdn.microsoft.com/bea5ba9c-538b-453f-ae6d-12b94b8edeb6">CVssWriterEx2::GetSessionId</a>, <a href="https://msdn.microsoft.com/9fef9d77-dc0d-4ba0-a317-5c62355458f7">CVssWriter::SetWriterFailure</a>, or <a href="https://msdn.microsoft.com/c049a016-6546-4e72-90e8-46be8c2f7764">CVssWriterEx2::SetWriterFailureEx</a> method, it must do so in  the same thread that called this method. For more information, see 
<a href="https://www.bing.com/search?q=Writer+Event+Handling">Writer Event Handling</a>.




## -see-also




<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a>



<a href="https://msdn.microsoft.com/77d0621d-81bd-4d53-8e5d-f5d3bfd86013">CVssWriter::OnBackupComplete</a>



<a href="https://msdn.microsoft.com/9fef9d77-dc0d-4ba0-a317-5c62355458f7">CVssWriter::SetWriterFailure</a>



<a href="https://msdn.microsoft.com/ee49d4b1-f3f4-4c85-a3a2-f4452d066f21">IVssBackupComponents::BackupComplete</a>
 

 

