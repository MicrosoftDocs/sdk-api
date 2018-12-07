---
UID: NF:vsbackup.IVssBackupComponents.PrepareForBackup
title: IVssBackupComponents::PrepareForBackup
author: windows-sdk-content
description: The PrepareForBackup method will cause VSS to generate a PrepareForBackup event, signaling writers to prepare for an upcoming backup operation. This makes a requester's Backup Components Document available to writers.
old-location: base\ivssbackupcomponents_prepareforbackup.htm
tech.root: vss
ms.assetid: 46ce8282-a434-4b0b-b66e-40810052b34b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVssBackupComponents interface [VSS],PrepareForBackup method, IVssBackupComponents.PrepareForBackup, IVssBackupComponents::PrepareForBackup, PrepareForBackup, PrepareForBackup method [VSS], PrepareForBackup method [VSS],IVssBackupComponents interface, _win32_ivssbackupcomponents_prepareforbackup, base.ivssbackupcomponents_prepareforbackup, vsbackup/IVssBackupComponents::PrepareForBackup
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
 - IVssBackupComponents.PrepareForBackup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVssBackupComponents::PrepareForBackup


## -description


The 
<b>PrepareForBackup</b> method will cause VSS to generate a 
<a href="https://msdn.microsoft.com/en-us/library/Aa384664(v=VS.85).aspx">PrepareForBackup</a> event, signaling writers to prepare for an upcoming backup operation. This makes a requester's Backup Components Document available to writers.


## -parameters




### -param ppAsync [out]

Doubly indirect pointer to an instance of the 
<a href="https://msdn.microsoft.com/d2cff547-b4ff-454d-8e0e-cd29b91cbb07">IVssAsync</a> interface that is used to determine when the asynchronous operation is complete.


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
<a href="https://msdn.microsoft.com/d2cff547-b4ff-454d-8e0e-cd29b91cbb07">IVssAsync</a> interface. See 
<a href="https://msdn.microsoft.com/85fb3ae8-dc09-4f6f-a96b-e4dc046ff48a">IVssAsync::QueryStatus</a> for the error codes returned in the <i>pHrResult</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppAsync</i> does not point to a valid pointer; that is, it is <b>NULL</b>.

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



<b>PrepareForBackup</b> generates a 
PrepareForBackup event, which is handled by each instance of each writer through the 
<a href="https://msdn.microsoft.com/4e88d92b-48f3-42f9-bf66-61337a745902">CVssWriter::OnPrepareBackup</a> method.

Before 
<b>PrepareForBackup</b> can be called, 
<a href="https://msdn.microsoft.com/18a1295d-b763-477b-bda2-baf8a878bf46">IVssBackupComponents::SetBackupState</a> must be called.

The Backup Components Document can still be modified by writers in their 
<b>PrepareForBackup</b> event handler (<a href="https://msdn.microsoft.com/4e88d92b-48f3-42f9-bf66-61337a745902">CVssWriter::OnPrepareBackup</a>), and afterward until the generation of a 
<a href="https://msdn.microsoft.com/ee49d4b1-f3f4-4c85-a3a2-f4452d066f21">BackupComplete</a> event.

The caller is responsible for releasing the 
<a href="https://msdn.microsoft.com/d2cff547-b4ff-454d-8e0e-cd29b91cbb07">IVssAsync</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/d2cff547-b4ff-454d-8e0e-cd29b91cbb07">IVssAsync</a>



<a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a>



<a href="https://msdn.microsoft.com/50cb0b16-9ed3-4496-962a-9c845c10986c">IVssBackupComponents::AddComponent</a>



<a href="https://msdn.microsoft.com/6c20e386-7cd8-45d9-92d6-96d0a458db50">IVssBackupComponents::AddToSnapshotSet</a>



<a href="https://msdn.microsoft.com/6a0a6228-2131-48a6-8d18-9491969d265b">IVssBackupComponents::StartSnapshotSet</a>



<a href="https://msdn.microsoft.com/c686a424-b0b9-4efc-8dc6-b92193de2a5d">IVssComponent</a>
 

 

