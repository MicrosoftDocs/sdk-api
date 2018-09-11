---
UID: NF:vsbackup.IVssBackupComponents.PreRestore
title: IVssBackupComponents::PreRestore
author: windows-sdk-content
description: The PreRestore method will cause VSS to generate a PreRestore event, signaling writers to prepare for an upcoming restore operation.
old-location: base\ivssbackupcomponents_prerestore.htm
tech.root: VSS
ms.assetid: 7a4c8869-9655-49a7-818b-98a08103f4b4
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IVssBackupComponents interface [VSS],PreRestore method, IVssBackupComponents.PreRestore, IVssBackupComponents::PreRestore, PreRestore, PreRestore method [VSS], PreRestore method [VSS],IVssBackupComponents interface, _win32_ivssbackupcomponents_prerestore, base.ivssbackupcomponents_prerestore, vsbackup/IVssBackupComponents::PreRestore
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IVssBackupComponents.PreRestore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVssBackupComponents::PreRestore


## -description


The 
<b>PreRestore</b> method will cause VSS to generate a 
<a href="https://msdn.microsoft.com/en-us/library/Aa384664(v=VS.85).aspx">PreRestore</a> event, signaling writers to prepare for an upcoming restore operation.


## -parameters




### -param ppAsync [out]

Doubly indirect pointer to an 
<a href="https://msdn.microsoft.com/d2cff547-b4ff-454d-8e0e-cd29b91cbb07">IVssAsync</a> object containing status data for the signaled event.


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
Successfully returned a pointer to an instance of the 
<a href="https://msdn.microsoft.com/d2cff547-b4ff-454d-8e0e-cd29b91cbb07">IVssAsync</a> interface. Refer to <a href="https://msdn.microsoft.com/85fb3ae8-dc09-4f6f-a96b-e4dc046ff48a">IVssAsync::QueryStatus</a> for the error codes returned in the <i>pHrResult</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppAsync</i> parameter does not point to a valid pointer; that is, it is <b>NULL</b>.

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



The caller is responsible for releasing the 
<a href="https://msdn.microsoft.com/d2cff547-b4ff-454d-8e0e-cd29b91cbb07">IVssAsync</a> interface pointer.

Special consideration should be given to EFI systems when the requester has selected the Automated System Recovery (ASR) writer for restore.  If you are restoring to a disk that contains the EFI partition, and one of the following conditions exists, you must first clean the disk by calling the <a href="https://msdn.microsoft.com/4052f294-d911-44c6-a57f-0a0a6f24df70">IVdsAdvancedDisk::Clean</a> method:

<ul>
<li>You are restoring to an EFI system disk whose partitioning has changed since the last ASR backup.</li>
<li>You are restoring to a different physical drive than the one from which the backup was taken.</li>
</ul>
Failure to perform this disk-cleaning step may result in unexpected results during <a href="https://msdn.microsoft.com/en-us/library/Aa384664(v=VS.85).aspx">PreRestore</a>.

For more information about the ASR writer, see <a href="https://msdn.microsoft.com/e20a303d-9440-42be-b383-85f6fad89157">In-Box VSS Writers</a>.




## -see-also




<a href="https://msdn.microsoft.com/d2cff547-b4ff-454d-8e0e-cd29b91cbb07">IVssAsync</a>



<a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a>
 

 

