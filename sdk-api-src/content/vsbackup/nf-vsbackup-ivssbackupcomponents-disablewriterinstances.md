---
UID: NF:vsbackup.IVssBackupComponents.DisableWriterInstances
title: IVssBackupComponents::DisableWriterInstances (vsbackup.h)
author: windows-sdk-content
description: The DisableWriterInstances method disables a specified writer instance or instances.
old-location: base\ivssbackupcomponents_disablewriterinstances.htm
tech.root: VSS
ms.assetid: 746fb12d-83d7-463d-848d-36e095832d1a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DisableWriterInstances, DisableWriterInstances method [VSS], DisableWriterInstances method [VSS],IVssBackupComponents interface, IVssBackupComponents interface [VSS],DisableWriterInstances method, IVssBackupComponents.DisableWriterInstances, IVssBackupComponents::DisableWriterInstances, _win32_ivssbackupcomponents_disablewriterinstances, base.ivssbackupcomponents_disablewriterinstances, vsbackup/IVssBackupComponents::DisableWriterInstances
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
 - IVssBackupComponents.DisableWriterInstances
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVssBackupComponents::DisableWriterInstances


## -description


The 
<b>DisableWriterInstances</b> method disables a specified writer instance or instances.


## -parameters




### -param rgWriterInstanceId [in]

An array containing one or more writer instance identifiers.


### -param cInstanceId [in]

The number of entries in the <i>rgWriterInstanceId</i> array.


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
The writer class has been successfully enabled.

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



If you have multiple running copies of the same writer, they will all have the same writer class identifier, but they will have different writer instance identifiers. Disabling one instance of a writer does not cause the writer's other instances to be disabled.

If you call <b>DisableWriterInstances</b>, you must do so before calling the <a href="https://msdn.microsoft.com/44f19c10-c966-4ab6-98dd-865d535955db">IVssBackupComponents::GatherWriterMetadata</a> method. If you call <b>GatherWriterMetadata</b> first and then call <b>DisableWriterInstances</b>, the call to <b>DisableWriterInstances</b> has no effect. If you need to call <b>GatherWriterMetadata</b> first, to determine which writer instances to disable, you must call it from a different instance of the <a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a>



<a href="https://msdn.microsoft.com/7567bf23-4f4c-4210-87f7-4f90262fda7a">IVssBackupComponents::DisableWriterClasses</a>



<a href="https://msdn.microsoft.com/27dae374-f3c4-44a5-a0d7-3edb647f0593">IVssBackupComponents::EnableWriterClasses</a>



<a href="https://msdn.microsoft.com/44f19c10-c966-4ab6-98dd-865d535955db">IVssBackupComponents::GatherWriterMetadata</a>
 

 

