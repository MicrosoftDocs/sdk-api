---
UID: NF:vswriter.CVssWriter.OnBackupComplete
title: CVssWriter::OnBackupComplete
author: windows-sdk-content
description: The OnBackupComplete method is called by a writer following a BackupComplete event. It is used to perform operations considered necessary following a backup. These operations cannot, however, modify the Backup Components Document.
old-location: base\cvsswriter_onbackupcomplete.htm
tech.root: vss
ms.assetid: 77d0621d-81bd-4d53-8e5d-f5d3bfd86013
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CVssWriter interface [VSS],OnBackupComplete method, CVssWriter.OnBackupComplete, CVssWriter::OnBackupComplete, OnBackupComplete, OnBackupComplete method [VSS], OnBackupComplete method [VSS],CVssWriter interface, _win32_cvsswriter_onbackupcomplete, base.cvsswriter_onbackupcomplete, vswriter/CVssWriter::OnBackupComplete
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CVssWriter::OnBackupComplete


## -description


The <b>OnBackupComplete</b> method is called by a 
    writer following a <a href="https://msdn.microsoft.com/ee49d4b1-f3f4-4c85-a3a2-f4452d066f21">BackupComplete</a> event. 
    It is used to perform operations considered necessary following a backup. These operations cannot, however, modify 
    the Backup Components Document.
   

<b>OnBackupComplete</b> is a virtual method. It is
   implemented by the <a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a> base class, but can be overridden 
   by derived classes.


## -parameters




### -param pComponent [in]

A pointer to an <a href="https://msdn.microsoft.com/e8ff2491-014c-43c7-bdce-99ed3b408605">IVssWriterComponents</a> object 
      passed in by VSS to provide the method with access to the writer's component information. The value of this 
      parameter may be <b>NULL</b> if the requester does not support components (if 
      <a href="https://msdn.microsoft.com/da84f1ab-8712-436f-8ae7-ba3d52a761c0">CVssWriter::AreComponentsSelected</a> returns
      <b>false</b>).
     


## -returns



As implemented by the base class, 
       <b>OnBackupComplete</b> always returns <b>true</b>.
      

Any other implementation of this method should return <b>true</b> except in the case of a fatal error.
      If a fatal error occurs, the method must call the <a href="https://msdn.microsoft.com/9fef9d77-dc0d-4ba0-a317-5c62355458f7">CVssWriter::SetWriterFailure</a> method to provide a description of the failure before returning <b>false</b>. If a nonfatal error occurs, the method should still call <b>SetWriterFailure</b> but return <b>true</b>. If the error is caused by a transient problem, the method should specify VSS_E_WRITERERROR_RETRYABLE in the call to <b>SetWriterFailure</b>.

  In all cases when a failure occurs, the method should write an event to the event log to report the exact reason for the failure.




## -remarks



The default implementation of this method by 
    <a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a> base class returns <b>true</b> without 
    performing any other operation.
   

If special operations are to be performed by the writer at the end of a backup, 
    the default implementation can be overridden.
   

With the generation of a 
    <a href="https://msdn.microsoft.com/ee49d4b1-f3f4-4c85-a3a2-f4452d066f21">BackupComplete</a> event, a 
    requester's Backup Components Document becomes a read-only document. Therefore, attempts to modify the 
    document through the interface (for instance, calling 
    <a href="https://msdn.microsoft.com/96d0a581-87a5-4f97-b23f-08e90a805de1">IVssComponent::SetBackupMetadata</a>) will 
    fail in user implementations of 
    <b>OnBackupComplete</b>.
   

A successful backup application will generate a 
    <a href="https://msdn.microsoft.com/ee49d4b1-f3f4-4c85-a3a2-f4452d066f21">BackupComplete</a> event when all data 
    has been saved to backup media.
   

However, there is no guarantee of the writer receiving a 
    <a href="https://msdn.microsoft.com/ee49d4b1-f3f4-4c85-a3a2-f4452d066f21">BackupComplete</a> event notification,
    because these require the backup application to either successfully complete the backup or fail gracefully.
   

A <a href="https://msdn.microsoft.com/ee49d4b1-f3f4-4c85-a3a2-f4452d066f21">BackupComplete</a> event could fail to 
    be generated should the backup application be terminated by the system or manually prior to the completion of the
    backup (for instance, if the backup operation hung and had to be shut down).
   

A writer should maintain state information so that it can track whether a 
    <a href="https://msdn.microsoft.com/ee49d4b1-f3f4-4c85-a3a2-f4452d066f21">BackupComplete</a> event was sent for a
    given shadow copy set.
   

This information can be used by a writer's 
    <a href="https://msdn.microsoft.com/en-us/library/Aa384652(v=VS.85).aspx">BackupShutdown</a> event handler 
    (<a href="https://msdn.microsoft.com/4b6d5efe-703b-4245-81d8-e2fc7f650d4b">CVssWriter::OnBackupShutdown</a>), 
    which will be called when a backup application actually terminates and its 
    <a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a> is released, to perform 
    cleanup operations should there be no call to 
    <b>OnBackupComplete</b>.
   

Writers should never throw an exception from this method or any other <b>CVssWriter(Ex)::On<i>Xxx</i></b> callback method.

If this method calls the <a href="https://msdn.microsoft.com/bea5ba9c-538b-453f-ae6d-12b94b8edeb6">CVssWriterEx2::GetSessionId</a>, <a href="https://msdn.microsoft.com/9fef9d77-dc0d-4ba0-a317-5c62355458f7">CVssWriter::SetWriterFailure</a>, or <a href="https://msdn.microsoft.com/c049a016-6546-4e72-90e8-46be8c2f7764">CVssWriterEx2::SetWriterFailureEx</a> method, it must do so in  the same thread that called this method. For more information, see 
<a href="https://msdn.microsoft.com/en-us/library/Aa384993(v=VS.85).aspx">Writer Event Handling</a>.




## -see-also




<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a>



<a href="https://msdn.microsoft.com/9fef9d77-dc0d-4ba0-a317-5c62355458f7">CVssWriter::SetWriterFailure</a>



<a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a>



<a href="https://msdn.microsoft.com/e8ff2491-014c-43c7-bdce-99ed3b408605">IVssWriterComponents</a>
 

 

