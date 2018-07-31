---
UID: NF:vswriter.CVssWriter.OnPostRestore
title: CVssWriter::OnPostRestore
author: windows-sdk-content
description: The OnPostRestore method is called by a writer following a PostRestore event. It is used to perform operations considered necessary after files are restored to disk by a requester. These operations cannot, however, modify the Backup Components Document.
old-location: base\cvsswriter_onpostrestore.htm
old-project: VSS
ms.assetid: ad07753c-1592-4fc8-9899-a73e798c158c
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: CVssWriter interface [VSS],OnPostRestore method, CVssWriter.OnPostRestore, CVssWriter::OnPostRestore, OnPostRestore, OnPostRestore method [VSS], OnPostRestore method [VSS],CVssWriter interface, _win32_cvsswriter_onpostrestore, base.cvsswriter_onpostrestore, vswriter/CVssWriter::OnPostRestore
ms.prod: windows
ms.technology: windows-sdk
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
 - CVssWriter.OnPostRestore
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# CVssWriter::OnPostRestore


## -description


The 
<b>OnPostRestore</b> method is called by a writer following a 
<a href="https://msdn.microsoft.com/01cf3931-59ef-4572-9f2e-aa210da0ac2d">PostRestore</a> event. It is used to perform operations considered necessary after files are restored to disk by a requester. These operations cannot, however, modify the Backup Components Document.

<b>OnPostRestore</b> is a virtual method. It is implemented by the 
<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a> base class, but can be overridden by derived classes.


## -parameters




### -param pComponent [in]

A pointer to an 
<a href="https://msdn.microsoft.com/e8ff2491-014c-43c7-bdce-99ed3b408605">IVssWriterComponents</a> object passed in by VSS to provide the method with access to the writer's component information. The value of this parameter may be <b>NULL</b> if the requester does not support components (if 
<a href="https://msdn.microsoft.com/da84f1ab-8712-436f-8ae7-ba3d52a761c0">CVssWriter::AreComponentsSelected</a> returns <b>false</b>).


## -returns



As implemented by the base class, 
<b>OnPostRestore</b> always returns <b>true</b>.

Any other implementation of this method must return <b>true</b> except in the case of a fatal error.
      If a fatal error occurs, the method must call the <a href="https://msdn.microsoft.com/9fef9d77-dc0d-4ba0-a317-5c62355458f7">CVssWriter::SetWriterFailure</a> method to provide a description of the failure before returning <b>false</b>. If a nonfatal error occurs, the method should still call <b>SetWriterFailure</b> but return <b>true</b>. If the error is caused by a transient problem, the method should specify VSS_E_WRITERERROR_RETRYABLE in the call to <b>SetWriterFailure</b>.

  In all cases when a failure occurs, the method should write an event to the event log to report the exact reason for the failure.




## -remarks



The default implementation of this method by the 
<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a> base class returns <b>true</b> without performing any other operation.

If necessary, a writer should remove any temporary files and release any system resources that it needed for its participation in the restore.

Writers should never throw an exception from this method or any other <b>CVssWriter(Ex)::On<i>Xxx</i></b> callback method.

With the generation of a 
<a href="https://msdn.microsoft.com/01cf3931-59ef-4572-9f2e-aa210da0ac2d">PostRestore</a> event, a requester's Backup Components Document becomes a read-only document. Therefore, attempts to modify the document through the interface (for instance, calling 
<a href="https://msdn.microsoft.com/2b329fa8-21ad-4de9-9857-52e14d51d429">IVssComponent::SetRestoreMetadata</a>) will fail in user implementations of 
<b>OnPostRestore</b>.

If this method calls the <a href="https://msdn.microsoft.com/bea5ba9c-538b-453f-ae6d-12b94b8edeb6">CVssWriterEx2::GetSessionId</a>, <a href="https://msdn.microsoft.com/9fef9d77-dc0d-4ba0-a317-5c62355458f7">CVssWriter::SetWriterFailure</a>, or <a href="https://msdn.microsoft.com/c049a016-6546-4e72-90e8-46be8c2f7764">CVssWriterEx2::SetWriterFailureEx</a> method, it must do so in  the same thread that called this method. For more information, see 
<a href="writers.htm">Writer Event Handling</a>.




## -see-also




<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a>



<a href="https://msdn.microsoft.com/e8ff2491-014c-43c7-bdce-99ed3b408605">IVssWriterComponents</a>
 

 

