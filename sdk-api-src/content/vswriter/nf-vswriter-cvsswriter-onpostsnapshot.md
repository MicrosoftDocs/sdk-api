---
UID: NF:vswriter.CVssWriter.OnPostSnapshot
title: CVssWriter::OnPostSnapshot
author: windows-sdk-content
description: The OnPostSnapshot method is called by a writer following a PostSnapshot event.
old-location: base\cvsswriter_onpostsnapshot.htm
tech.root: VSS
ms.assetid: d97d4246-882e-49c3-a214-d8d3887c1508
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CVssWriter class [VSS],OnPostSnapshot method, CVssWriter.OnPostSnapshot, CVssWriter::OnPostSnapshot, OnPostSnapshot, OnPostSnapshot method [VSS], OnPostSnapshot method [VSS],CVssWriter class, _win32_cvsswriter_onpostsnapshot, base.cvsswriter_onpostsnapshot, vswriter/CVssWriter::OnPostSnapshot
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
 - CVssWriter.OnPostSnapshot
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- vswriter.h
: 
- CVssWriter.OnPostSnapshot
: 
---

# CVssWriter::OnPostSnapshot


## -description


The <b>OnPostSnapshot</b> method is called by a 
    writer following a <a href="https://msdn.microsoft.com/en-us/library/Aa384664(v=VS.85).aspx">PostSnapshot</a> 
    event.

<b>OnPostSnapshot</b> is a virtual method. It is 
    implemented by the <a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a> base class but can be 
    overridden by derived classes.


## -parameters




### -param pComponent [in]

A pointer to an <a href="https://msdn.microsoft.com/e8ff2491-014c-43c7-bdce-99ed3b408605">IVssWriterComponents</a> object 
      passed in by VSS to provide the method with access to the writer's component information. The value of this 
      parameter may be NULL if the requester does not support components (if 
      <a href="https://msdn.microsoft.com/da84f1ab-8712-436f-8ae7-ba3d52a761c0">CVssWriter::AreComponentsSelected</a> 
      returns <b>false</b>).


## -returns



As implemented by the base class, 
       <b>OnPostSnapshot</b> always returns <b>true</b>.

Any other implementation of this method must return <b>true</b> except in the case of a fatal error.
      If a fatal error occurs, the method must call the <a href="https://msdn.microsoft.com/9fef9d77-dc0d-4ba0-a317-5c62355458f7">CVssWriter::SetWriterFailure</a> method to provide a description of the failure before returning <b>false</b>. If a nonfatal error occurs, the method should still call <b>SetWriterFailure</b> but return <b>true</b>. If the error is caused by a transient problem, the method should specify VSS_E_WRITERERROR_RETRYABLE in the call to <b>SetWriterFailure</b>.

  In all cases when a failure occurs, the method should write an event to the event log to report the exact reason for the failure.




## -remarks



The default implementation of this method by the 
    <a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a> base class returns <b>true</b> without 
    performing any other operation.

<b>CVssWriter::OnPostSnapshot</b> is typically 
       used to process any final updates by the writer to the backup components metadata and clean up (such as 
       removing temporary files).

If an incremental or differential backup is being performed, the writer may call <a href="https://msdn.microsoft.com/91778854-52af-4e1e-943b-89c786963291">IVssComponent::GetPreviousBackupStamp</a> and <a href="https://msdn.microsoft.com/54995cc9-8988-4f26-9c60-5d809a93e4e1">IVssComponent::SetBackupStamp</a>. For more information, see <a href="https://msdn.microsoft.com/3cf5dd1f-dc58-42bc-925f-fee7d34053c5">Writer Role in Backing Up Complex Stores</a>. Another method that can be called at this time is <a href="https://msdn.microsoft.com/33372d10-c947-45de-9ea2-03ba6378179d">IVssComponent::AddDifferencedFilesByLastModifyTime</a>.

Most of the work needed to return the writer to normal operation (reversing the actions of 
       <a href="https://msdn.microsoft.com/a077323e-d04c-4bf7-8aa6-5028fa1c6e6b">CVssWriter::OnPrepareSnapshot</a> and 
       <a href="https://msdn.microsoft.com/2aff5e87-4053-46a0-a7fb-7411e76166ba">CVssWriter::OnFreeze</a>) is typically performed in 
       <a href="https://msdn.microsoft.com/36028e9f-f7a7-41f1-a570-48f943e9ab83">CVssWriter::OnThaw</a>, not in 
       <b>OnPostSnapshot</b>.

Writers should never throw an exception from this method or any other <b>CVssWriter(Ex)::On<i>Xxx</i></b> callback method.

 If the shadow copy has the <b>VSS_VOLSNAP_ATTR_AUTORECOVER</b> flag set in the context, 
    the writer should perform any recovery required (for example, rolling back any incomplete transactions) so that 
    the component will be usable on a read-only copy for data mining (without adding load to the live server) or 
    restore purposes (for example, to restore selected items from a database).

To retrieve the volume name of the shadow copy of a volume, perform the following steps:

<ol>
<li>Call the <a href="https://msdn.microsoft.com/5f553a46-10ee-475e-b028-2652c74fbe5d">CVssWriter::GetCurrentVolumeCount</a> method to query the number of volumes in the shadow copy set.</li>
<li>Call the <a href="https://msdn.microsoft.com/75f72b51-e940-4b1d-88a1-7c35de5a3d87">CVssWriter::GetCurrentVolumeArray</a> method to enumerate the original names of the volumes in the shadow copy set.</li>
<li>Call the <a href="https://msdn.microsoft.com/ac0beefe-0afd-45da-b1bb-1bd960b4b0f0">CVssWriter::GetSnapshotDeviceName</a> to retrieve the name of the shadow copy volume.</li>
</ol>
If this method calls the <a href="https://msdn.microsoft.com/bea5ba9c-538b-453f-ae6d-12b94b8edeb6">CVssWriterEx2::GetSessionId</a>, <a href="https://msdn.microsoft.com/9fef9d77-dc0d-4ba0-a317-5c62355458f7">CVssWriter::SetWriterFailure</a>, or <a href="https://msdn.microsoft.com/c049a016-6546-4e72-90e8-46be8c2f7764">CVssWriterEx2::SetWriterFailureEx</a> method, it must do so in  the same thread that called this method. For more information, see 
<a href="https://msdn.microsoft.com/en-us/library/Aa384993(v=VS.85).aspx">Writer Event Handling</a>.




## -see-also




<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a>



<a href="https://msdn.microsoft.com/ac0beefe-0afd-45da-b1bb-1bd960b4b0f0">CVssWriter::GetSnapshotDeviceName</a>



<a href="https://msdn.microsoft.com/5f4a6168-4102-4790-81d6-d195a440471f">CVssWriter::OnPreRestore</a>



<a href="https://msdn.microsoft.com/4e88d92b-48f3-42f9-bf66-61337a745902">CVssWriter::OnPrepareBackup</a>



<a href="https://msdn.microsoft.com/9fef9d77-dc0d-4ba0-a317-5c62355458f7">CVssWriter::SetWriterFailure</a>



<a href="https://msdn.microsoft.com/36028e9f-f7a7-41f1-a570-48f943e9ab83">CvssWriter::OnThaw</a>



<a href="https://msdn.microsoft.com/e8ff2491-014c-43c7-bdce-99ed3b408605">IVssWriterComponents</a>
 

 

