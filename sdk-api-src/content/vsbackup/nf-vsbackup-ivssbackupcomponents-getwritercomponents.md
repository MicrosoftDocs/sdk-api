---
UID: NF:vsbackup.IVssBackupComponents.GetWriterComponents
title: IVssBackupComponents::GetWriterComponents
author: windows-sdk-content
description: The GetWriterComponents method is used to return information about those components of a given writer that have been stored in a requester's Backup Components Document.
old-location: base\ivssbackupcomponents_getwritercomponents.htm
old-project: VSS
ms.assetid: b99e7e41-1c88-462c-b6d8-734f7a6e24d4
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetWriterComponents, GetWriterComponents method [VSS], GetWriterComponents method [VSS],IVssBackupComponents interface, IVssBackupComponents interface [VSS],GetWriterComponents method, IVssBackupComponents.GetWriterComponents, IVssBackupComponents::GetWriterComponents, _win32_ivssbackupcomponents_getwritercomponents, base.ivssbackupcomponents_getwritercomponents, vsbackup/IVssBackupComponents::GetWriterComponents
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
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
req.typenames: AMVPSIZE, *LPAMVPSIZE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	VssApi.lib
-	VssApi.dll
api_name:
-	IVssBackupComponents.GetWriterComponents
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssBackupComponents::GetWriterComponents


## -description


The 
<b>GetWriterComponents</b> method is used to return information about those components of a given writer that have been stored in a requester's Backup Components Document.


## -parameters




### -param iWriter [in]

The index of the writer being queried. It is a number between 0 and <i>n</i>-1, where <i>n</i> is the value returned by 
<a href="https://msdn.microsoft.com/39ab6179-2828-46dc-bfcd-0dd62c34ce95">IVssBackupComponents::GetWriterComponentsCount</a>.


### -param ppWriter






#### - pWriterComponents [out]

Doubly indirect pointer to an 
<a href="https://msdn.microsoft.com/29772c1f-1cc4-4ee7-8e1d-f1a6cbebf470">IVssWriterComponentsExt</a> interface object that will receive the returned component information.


## -returns



The following are the valid return codes for this method.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Successfully returned a pointer to an 
<a href="https://msdn.microsoft.com/29772c1f-1cc4-4ee7-8e1d-f1a6cbebf470">IVssWriterComponentsExt</a> interface object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameter values is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The caller is out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_BAD_STATE</b></dt>
</dl>
</td>
<td width="60%">
The backup components object is not initialized, this method has been called during a restore operation, or this method has not been called within the correct sequence.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified shadow copy does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">

        Unexpected error. The error code is logged in the error log file. For more information, see 
        <a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
</table>
 




## -remarks



The caller of this method must call <a href="_com_iunknown_release">IUnknown::Release</a> when it finishes accessing the component information.

<b>GetWriterComponents</b> retrieves component information for a component stored in the Backup Components Document by earlier calls to 
<a href="https://msdn.microsoft.com/50cb0b16-9ed3-4496-962a-9c845c10986c">IVssBackupComponents::AddComponent</a>.

The information in the components stored in the Backup Components Document is not static. If a writer updates a component during a restore, that change will be reflected in the component retrieved by 
<b>GetWriterComponents</b>. This is in contrast with component information found in the 
<a href="https://msdn.microsoft.com/8567ca7f-dc50-4cf2-b3c1-a2ae8d55dc95">IVssWMComponent</a> object returned by 
<a href="https://msdn.microsoft.com/fd03ac7c-8398-4972-85f1-2afe13317950">IVssExamineWriterMetadata::GetComponent</a>. That information is read-only and comes from the Writer Metadata Document of a writer process.

The <a href="https://msdn.microsoft.com/29772c1f-1cc4-4ee7-8e1d-f1a6cbebf470">IVssWriterComponentsExt</a> interface pointer that is returned in the <i>pWriterComponents</i> parameter should not be cached, because the following <a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a> methods cause the interface pointer that is returned by <b>GetWriterComponents</b> to be no longer valid:

<a href="https://msdn.microsoft.com/46ce8282-a434-4b0b-b66e-40810052b34b">IVssBackupComponents::PrepareForBackup</a>
<a href="https://msdn.microsoft.com/3cc6c375-8a24-4af3-b4ad-5a695cc2645c">IVssBackupComponents::DoSnapshotSet</a>
<a href="https://msdn.microsoft.com/ee49d4b1-f3f4-4c85-a3a2-f4452d066f21">IVssBackupComponents::BackupComplete</a>
<a href="https://msdn.microsoft.com/7a4c8869-9655-49a7-818b-98a08103f4b4">IVssBackupComponents::PreRestore</a>
<a href="https://msdn.microsoft.com/01cf3931-59ef-4572-9f2e-aa210da0ac2d">IVssBackupComponents::PostRestore</a>
If you call one of these methods after you have retrieved an <a href="https://msdn.microsoft.com/29772c1f-1cc4-4ee7-8e1d-f1a6cbebf470">IVssWriterComponentsExt</a> interface pointer by calling <b>GetWriterComponents</b>, you cannot reuse that pointer, because it is no longer valid. Instead, you must call <b>GetWriterComponents</b> again to retrieve a new <b>IVssWriterComponentsExt</b> interface pointer.




## -see-also




<a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a>



<a href="https://msdn.microsoft.com/50cb0b16-9ed3-4496-962a-9c845c10986c">IVssBackupComponents::AddComponent</a>



<a href="https://msdn.microsoft.com/44f19c10-c966-4ab6-98dd-865d535955db">IVssBackupComponents::GatherWriterMetadata</a>



<a href="https://msdn.microsoft.com/39ab6179-2828-46dc-bfcd-0dd62c34ce95">IVssBackupComponents::GetWriterComponentsCount</a>



<a href="https://msdn.microsoft.com/a577d06a-4c9d-4ebe-b4d4-685f96ec9c83">IVssBackupComponents::GetWriterMetadata</a>



<a href="https://msdn.microsoft.com/7a4c8869-9655-49a7-818b-98a08103f4b4">IVssBackupComponents::PreRestore</a>



<a href="https://msdn.microsoft.com/b3aa04d9-7299-4e3a-b092-d07f2de6eefe">IVssExamineWriterMetadata</a>



<a href="https://msdn.microsoft.com/fd03ac7c-8398-4972-85f1-2afe13317950">IVssExamineWriterMetadata::GetComponent</a>



<a href="https://msdn.microsoft.com/e8ff2491-014c-43c7-bdce-99ed3b408605">IVssWriterComponents</a>



<a href="https://msdn.microsoft.com/29772c1f-1cc4-4ee7-8e1d-f1a6cbebf470">IVssWriterComponentsExt</a>
 

 

