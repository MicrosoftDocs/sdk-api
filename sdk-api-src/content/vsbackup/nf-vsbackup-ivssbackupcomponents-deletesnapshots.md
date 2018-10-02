---
UID: NF:vsbackup.IVssBackupComponents.DeleteSnapshots
title: IVssBackupComponents::DeleteSnapshots
author: windows-sdk-content
description: The DeleteSnapshots method deletes one or more shadow copies or a shadow copy set.
old-location: base\ivssbackupcomponents_deletesnapshots.htm
tech.root: VSS
ms.assetid: 2e06f69e-8210-4773-8080-5c58e6f59792
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DeleteSnapshots, DeleteSnapshots method [VSS], DeleteSnapshots method [VSS],IVssBackupComponents interface, IVssBackupComponents interface [VSS],DeleteSnapshots method, IVssBackupComponents.DeleteSnapshots, IVssBackupComponents::DeleteSnapshots, _win32_ivssbackupcomponents_deletesnapshots, base.ivssbackupcomponents_deletesnapshots, vsbackup/IVssBackupComponents::DeleteSnapshots
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
 - IVssBackupComponents.DeleteSnapshots
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVssBackupComponents::DeleteSnapshots


## -description


The <b>DeleteSnapshots</b> method deletes 
    one or more shadow copies or a shadow copy set.
   


## -parameters




### -param SourceObjectId [in]

Identifier of the shadow copy or a shadow copy set to be deleted.


### -param eSourceObjectType [in]

Type of the object on which all shadow copies will be deleted. The value of this parameter is
      <b>VSS_OBJECT_SNAPSHOT</b> or <b>VSS_OBJECT_SNAPSHOT_SET</b>.
     


### -param bForceDelete [in]

If the value of this parameter is <b>TRUE</b>, the provider will do everything possible to delete the shadow copy or 
      shadow copies in a shadow copy set. If it is <b>FALSE</b>, no additional effort will be made.
     


### -param plDeletedSnapshots [out]

Number of deleted shadow copies.


### -param pNondeletedSnapshotID [out]

If an error occurs, the value of this parameter is the identifier of the first shadow copy that could not be 
      deleted. Otherwise, it is <b>GUID_NULL</b>.
     


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
The shadow copies were successfully deleted.

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
<dt><b>VSS_E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error. The error code is logged in the error log file. For more information, see 
        <a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

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
<dt><b>VSS_E_PROVIDER_VETO</b></dt>
</dl>
</td>
<td width="60%">
Expected provider error. The provider logged the error in the event log. For more information, see 
        <a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.
       

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_UNEXPECTED_PROVIDER_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Unexpected provider error. The error code is logged in the error log. For more information, see 
        <a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.
       

</td>
</tr>
</table>
 




## -remarks



Multiple shadow copies in a shadow copy set are deleted sequentially. If an error occurs during one of these 
    individual deletions, 
    <b>DeleteSnapshots</b> will return
    immediately; no attempt will be made to delete any remaining shadow copies. The 
    <a href="https://msdn.microsoft.com/e64b36d6-4f10-42bd-9ad4-00aba90e9715">VSS_ID</a> of the undeleted shadow copy is 
    returned in <i>pNondeletedSnapshotID</i>.
   

The requester is responsible for serializing the delete shadow copy operation.

During a backup, shadow copies are automatically released as soon as the 
    <a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a> instance is released. In this 
    case, it is not necessary to explicitly delete shadow copies.
   




## -see-also




<a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a>



<a href="https://msdn.microsoft.com/6a0a6228-2131-48a6-8d18-9491969d265b">IVssBackupComponents::StartSnapshotSet</a>



<a href="https://msdn.microsoft.com/e64b36d6-4f10-42bd-9ad4-00aba90e9715">VSS_ID</a>
 

 

