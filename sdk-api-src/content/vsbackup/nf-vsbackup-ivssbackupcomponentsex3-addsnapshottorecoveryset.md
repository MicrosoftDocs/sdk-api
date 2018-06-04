---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IVssBackupComponentsEx3::AddSnapshotToRecoverySet


## -description


Specifies the volumes to be included in a LUN resynchronization operation. This method is supported only on Windows server operating systems.


## -parameters




### -param snapshotId [in]

The identifier of the shadow copy that was returned by the <a href="https://msdn.microsoft.com/6c20e386-7cd8-45d9-92d6-96d0a458db50">IVssBackupComponents::AddToSnapshotSet</a> method during backup. This parameter is required and cannot be GUID_NULL.




### -param dwFlags [in]

This parameter is reserved and must be zero.


### -param pwszDestinationVolume [in, optional]

This parameter is optional and can be <b>NULL</b>. A value of <b>NULL</b> means that the contents of the shadow copy volume are to be copied back to the original volume. VSS identifies the original volume by the VDS_LUN_INFO information in the Backup Components Document.


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
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_BAD_STATE</b></dt>
<dt>0x80042301L</dt>
</dl>
</td>
<td width="60%">
Either there is no hardware provider that supports the operation, or the requester did not successfully add any volumes to the recovery set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_LEGACY_PROVIDER</b></dt>
<dt>0x800423F7L</dt>
</dl>
</td>
<td width="60%">
This version of the hardware provider does not support this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
<dt>0x80042308L</dt>
</dl>
</td>
<td width="60%">
The <i>snapshotId</i> parameter specifies a shadow copy that the hardware provider does not own.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_RESYNC_IN_PROGRESS</b></dt>
<dt>0x800423FFL</dt>
</dl>
</td>
<td width="60%">
Another LUN resynchronization operation is already in progress.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_SNAPSHOT_NOT_IN_SET</b></dt>
<dt>0x8004232BL</dt>
</dl>
</td>
<td width="60%">
The <i>snapshotId</i> parameter specifies a shadow copy that does not exist in the Backup Components Document.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_VOLUME_NOT_SUPPORTED</b></dt>
<dt>0x8004230CL</dt>
</dl>
</td>
<td width="60%">
LUN resynchronization is not supported on this volume, because it is a dynamic volume, because the destination disk does not have a unique page 83 storage identifier, because the specified volume does not reside on a LUN managed by a VSS hardware provider, or because the destination disk is a cluster quorum disk. 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/56c8e7c2-2d94-4674-bd20-bf036991474f">IVssBackupComponentsEx3</a>
 

 

