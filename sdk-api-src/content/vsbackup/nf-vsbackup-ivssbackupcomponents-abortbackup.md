---
UID: NF:vsbackup.IVssBackupComponents.AbortBackup
title: IVssBackupComponents::AbortBackup
author: windows-sdk-content
description: The AbortBackup method notifies VSS that a backup operation was terminated.
old-location: base\ivssbackupcomponents_abortbackup.htm
old-project: vss
ms.assetid: e854ab83-9a1a-4660-8a3e-37747b1b7d8c
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: AbortBackup, AbortBackup method [VSS], AbortBackup method [VSS],IVssBackupComponents interface, IVssBackupComponents interface [VSS],AbortBackup method, IVssBackupComponents.AbortBackup, IVssBackupComponents::AbortBackup, _win32_ivssbackupcomponents_abortbackup, base.ivssbackupcomponents_abortbackup, vsbackup/IVssBackupComponents::AbortBackup
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssBackupComponents.AbortBackup
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssBackupComponents::AbortBackup


## -description


The 
<b>AbortBackup</b> method notifies VSS that a backup operation was terminated.

This method must be called if a backup operation terminates after the creation of a shadow copy set with 
<a href="https://msdn.microsoft.com/6a0a6228-2131-48a6-8d18-9491969d265b">IVssBackupComponents::StartSnapshotSet</a> and before 
<a href="https://msdn.microsoft.com/3cc6c375-8a24-4af3-b4ad-5a695cc2645c">IVssBackupComponents::DoSnapshotSet</a> returns.

If 
<b>AbortBackup</b> is called and no shadow copy or backup operations are underway, it is ignored.


## -parameters






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
The query operation was successful.

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
The backup components object is not initialized.

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



<b>AbortBackup</b> generates an <a href="vssgloss_a.htm">Abort</a> event, which is handled by each instance of each writer through the 
<a href="https://msdn.microsoft.com/56ba5f08-4803-4137-9edd-ce05bc19773b">CVssWriter::OnAbort</a> method.




## -see-also




<a href="https://msdn.microsoft.com/8ab44737-114b-4edc-a097-d0fa297f6276">IVssAsync::Cancel</a>



<a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a>



<a href="https://msdn.microsoft.com/ee49d4b1-f3f4-4c85-a3a2-f4452d066f21">IVssBackupComponents::BackupComplete</a>



<a href="https://msdn.microsoft.com/3cc6c375-8a24-4af3-b4ad-5a695cc2645c">IVssBackupComponents::DoSnapshotSet</a>



<a href="https://msdn.microsoft.com/46ce8282-a434-4b0b-b66e-40810052b34b">IVssBackupComponents::PrepareForBackup</a>



<a href="https://msdn.microsoft.com/6a0a6228-2131-48a6-8d18-9491969d265b">IVssBackupComponents::StartSnapshotSet</a>
 

 

