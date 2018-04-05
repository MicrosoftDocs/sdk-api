---
UID: NF:vsbackup.IVssBackupComponents.ImportSnapshots
title: IVssBackupComponents::ImportSnapshots method
author: windows-driver-content
description: Imports shadow copies transported from a different machine.
old-location: base\ivssbackupcomponents_importsnapshots.htm
old-project: VSS
ms.assetid: 7f28c841-5448-4ed7-b76e-0aa5376fd8bf
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IVssBackupComponents, IVssBackupComponents interface [VSS], ImportSnapshots method, IVssBackupComponents::ImportSnapshots, ImportSnapshots method [VSS], ImportSnapshots method [VSS], IVssBackupComponents interface, ImportSnapshots,IVssBackupComponents.ImportSnapshots, _win32_ivssbackupcomponents_importsnapshots, base.ivssbackupcomponents_importsnapshots, vsbackup/IVssBackupComponents::ImportSnapshots
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1, Windows Server 2003 Datacenter, Windows Server 2003 Enterprise [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
-	IVssBackupComponents.ImportSnapshots
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssBackupComponents::ImportSnapshots method


## -description


The <b>ImportSnapshots</b> method 
    imports shadow copies transported from a different machine.<div class="alert"><b>Note</b>  This method is supported only on Windows Server operating systems and for Volume Shadow Copy Service  hardware providers.</div>
<div> </div>



## -parameters




### -param ppAsync [out]

Doubly indirect pointer to an <a href="https://msdn.microsoft.com/d2cff547-b4ff-454d-8e0e-cd29b91cbb07">IVssAsync</a> object 
      containing the imported shadow copy status data.


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
        <a href="https://msdn.microsoft.com/d2cff547-b4ff-454d-8e0e-cd29b91cbb07">IVssAsync</a> interface. Refer to the reference page for 
        <a href="https://msdn.microsoft.com/85fb3ae8-dc09-4f6f-a96b-e4dc046ff48a">IVssAsync::QueryStatus</a> for the error codes 
        returned in the <i>pHrResult</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient backup privileges or is not an administrator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppAsync</i> parameter does not point to a valid pointer; that is, it is 
        <b>NULL</b>.

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
The backup components object is not initialized, this method has been called during a restore operation, 
        or this method has not been called from within the correct sequence.

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



Only one shadow copy can be imported at a time. 

The requester is responsible for serializing the import shadow copy operation.

The caller is responsible for releasing the <a href="https://msdn.microsoft.com/d2cff547-b4ff-454d-8e0e-cd29b91cbb07">IVssAsync</a> 
    interface.

For more information on importing shadow copies, see 
    <a href="https://msdn.microsoft.com/4ec63917-03c0-434e-892e-3d9d4c47740e">Importing Transportable Shadow 
    Copied Volumes</a>.

<b>Transportable shadow copies in a cluster:  </b>For details about using transportable shadow copies in a cluster, see 
     <a href="https://msdn.microsoft.com/2eaffcf7-01b2-44ce-8bc4-fd9fa42c8a8c">Fast Recovery Using 
     Transportable Shadow Copied Volumes</a>. The transportable shadow copy must be 
     imported from outside the cluster as long as the original volume is mounted within the cluster.

<div class="alert"><b>Note</b>   If the shadow copy import fails, the Volume Shadow Copy Service won't clean up LUNs on it's own. The requester has to initiate the cleanup of LUNs.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/d2cff547-b4ff-454d-8e0e-cd29b91cbb07">IVssAsync</a>



<a href="https://msdn.microsoft.com/85fb3ae8-dc09-4f6f-a96b-e4dc046ff48a">IVssAsync::QueryStatus</a>



<a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a>



<a href="https://msdn.microsoft.com/5a0abafa-d770-4529-90e4-0c597729d525">IVssBackupComponents::ExposeSnapshot</a>



<a href="https://msdn.microsoft.com/df469964-c954-4f79-b88f-a521157a0c66">IVssBackupComponents::InitializeForBackup</a>
 

 

