---
UID: NF:vsprov.IVssFileShareSnapshotProvider.IsPathSnapshotted
title: IVssFileShareSnapshotProvider::IsPathSnapshotted
author: windows-driver-content
description: Determines whether the given Universal Naming Convention (UNC) path currently has any snapshots.
old-location: base\ivssfilesharesnapshotprovider_ispathsnapshotted.htm
old-project: VSS
ms.assetid: 9a885d5d-a441-4567-b562-39820fa7ffc1
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: IVssFileShareSnapshotProvider interface [VSS],IsPathSnapshotted method, IVssFileShareSnapshotProvider.IsPathSnapshotted, IVssFileShareSnapshotProvider::IsPathSnapshotted, IsPathSnapshotted, IsPathSnapshotted method [VSS], IsPathSnapshotted method [VSS],IVssFileShareSnapshotProvider interface, base.ivssfilesharesnapshotprovider_ispathsnapshotted, vsprov/IVssFileShareSnapshotProvider::IsPathSnapshotted
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vsprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VSS_MGMT_OBJECT_UNION, *PVSS_MGMT_OBJECT_UNION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	VssApi.lib
-	VssApi.dll
api_name:
-	IVssFileShareSnapshotProvider.IsPathSnapshotted
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssFileShareSnapshotProvider::IsPathSnapshotted


## -description



Determines whether the given Universal Naming Convention (UNC) path currently has any snapshots.




## -parameters




### -param pwszSharePath [in]

The path to the file share.


### -param pbSnapshotsPresent [out]

This parameter receives <b>TRUE</b> if the volume has a shadow copy, or <b>FALSE</b> if the volume does not have a shadow copy.


### -param plSnapshotCompatibility [out]

A bitmask of <a href="https://msdn.microsoft.com/105d7bd6-0e95-4803-ae39-f03af40daa8e">VSS_SNAPSHOT_COMPATIBILITY</a> values that indicate whether certain volume control or file I/O operations are disabled for the given volume, if the volume has a shadow copy.


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
The requested information was successfully returned.

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
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified volume was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_PROVIDER_VETO</b></dt>
</dl>
</td>
<td width="60%">

        Provider error. The provider logged the error in the event log. For more information, see 
        <a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.
       

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
 




## -see-also




<a href="https://msdn.microsoft.com/1af45503-2f6f-4266-a0d2-ffc74a7be16f">IVssFileShareSnapshotProvider</a>
 

 

