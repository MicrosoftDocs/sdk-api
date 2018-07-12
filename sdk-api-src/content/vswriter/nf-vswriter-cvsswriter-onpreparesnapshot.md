---
UID: NF:vswriter.CVssWriter.OnPrepareSnapshot
title: CVssWriter::OnPrepareSnapshot
author: windows-sdk-content
description: The OnPrepareSnapshot method is called by a writer to handle a PrepareForSnapshot event. It is used to perform operations needed to prepare a writer to participate in the shadow copy or to veto a shadow copy.
old-location: base\cvsswriter_onpreparesnapshot.htm
old-project: vss
ms.assetid: a077323e-d04c-4bf7-8aa6-5028fa1c6e6b
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: CVssWriter interface [VSS],OnPrepareSnapshot method, CVssWriter.OnPrepareSnapshot, CVssWriter::OnPrepareSnapshot, OnPrepareSnapshot, OnPrepareSnapshot method [VSS], OnPrepareSnapshot method [VSS],CVssWriter interface, _win32_cvsswriter_onpreparesnapshot, base.cvsswriter_onpreparesnapshot, vswriter/CVssWriter::OnPrepareSnapshot
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
 - CVssWriter.OnPrepareSnapshot
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# CVssWriter::OnPrepareSnapshot


## -description


The 
<b>OnPrepareSnapshot</b> method is called by a writer to handle a <a href="https://msdn.microsoft.com/library/Aa384664(v=VS.85).aspx">PrepareForSnapshot</a> event. It is used to perform operations needed to prepare a writer to participate in the shadow copy or to veto a shadow copy.

<b>OnPrepareSnapshot</b> is a pure virtual method. It is not implemented by the 
<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a> base class, and must be implemented by derived classes.


## -parameters






## -returns



The implementation of this method must return <b>true</b> except in the case of a fatal error.
      If a fatal error occurs, the method must call the <a href="https://msdn.microsoft.com/9fef9d77-dc0d-4ba0-a317-5c62355458f7">CVssWriter::SetWriterFailure</a> method to provide a description of the failure before returning <b>false</b>. If a nonfatal error occurs, the method should still call  <b>SetWriterFailure</b> but return <b>true</b>. If the error is caused by a transient problem, the method should specify VSS_E_WRITERERROR_RETRYABLE in the call to <b>SetWriterFailure</b>.

  In all cases when a failure occurs, the method should write an event to the event log to report the exact reason for the failure.




## -remarks



The 
<b>OnPrepareSnapshot</b> method performs operations that are required prior to any shadow copy freeze.

The time-out window for handling a <a href="https://msdn.microsoft.com/library/Aa384664(v=VS.85).aspx">PrepareForSnapshot</a> event is typically longer than that for handling a <a href="https://msdn.microsoft.com/library/Aa384656(v=VS.85).aspx">Freeze</a> event. Therefore, developers can use 
<b>OnPrepareSnapshot</b> to handle more time-consuming operations. A typical use might be for the writer to explicitly checkpoint its data.

Writers should never throw an exception from this method or any other <b>CVssWriter(Ex)::On<i>Xxx</i></b> callback method.

If this method calls the <a href="https://msdn.microsoft.com/bea5ba9c-538b-453f-ae6d-12b94b8edeb6">CVssWriterEx2::GetSessionId</a>, <a href="https://msdn.microsoft.com/9fef9d77-dc0d-4ba0-a317-5c62355458f7">CVssWriter::SetWriterFailure</a>, or <a href="https://msdn.microsoft.com/c049a016-6546-4e72-90e8-46be8c2f7764">CVssWriterEx2::SetWriterFailureEx</a> method, it must do so in  the same thread that called this method. For more information, see 
<a href="https://msdn.microsoft.com/library/Aa384993(v=VS.85).aspx">Writer Event Handling</a>.




## -see-also




<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a>



<a href="https://msdn.microsoft.com/56ba5f08-4803-4137-9edd-ce05bc19773b">CVssWriter::OnAbort</a>



<a href="https://msdn.microsoft.com/2aff5e87-4053-46a0-a7fb-7411e76166ba">CVssWriter::OnFreeze</a>



<a href="https://msdn.microsoft.com/36028e9f-f7a7-41f1-a570-48f943e9ab83">CVssWriter::OnThaw</a>



<a href="https://msdn.microsoft.com/9fef9d77-dc0d-4ba0-a317-5c62355458f7">CVssWriter::SetWriterFailure</a>
 

 

