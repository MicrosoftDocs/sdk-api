---
UID: NF:iscsidsc.AddPersistentIScsiDeviceW
title: AddPersistentIScsiDeviceW function
author: windows-sdk-content
description: AddPersistentIscsiDevice function adds a volume device name, drive letter, or mount point symbolic link to the list of iSCSI persistently bound volumes and devices.
old-location: iscsidisc\addpersistentiscsidevice.htm
old-project: iSCSIDisc
ms.assetid: 184b256b-0cb0-45c1-8f73-5ff28fb388fb
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AddPersistentIScsiDeviceW, AddPersistentIscsiDevice, AddPersistentIscsiDevice function [iSCSI Discovery Library API], AddPersistentIscsiDeviceA, AddPersistentIscsiDeviceW, AddPersistentiScsiDevice, iscsidisc.addpersistentiscsidevice, iscsidsc/AddPersistentIscsiDevice, iscsidsc/AddPersistentIscsiDeviceA, iscsidsc/AddPersistentIscsiDeviceW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: AddPersistentIscsiDeviceW (Unicode) and AddPersistentIscsiDeviceA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TARGET_INFORMATION_CLASS, *PTARGET_INFORMATION_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iscsidsc.dll
api_name:
 - AddPersistentIscsiDevice
 - AddPersistentIscsiDeviceA
 - AddPersistentIscsiDeviceW
product: Windows
targetos: Windows
req.lib: Iscsidsc.lib
req.dll: Iscsidsc.dll
req.irql: 
req.product: GDI+ 1.1
---

# AddPersistentIScsiDeviceW function


## -description


The <b>AddPersistentIscsiDevice</b> function adds a volume device name, drive letter, or mount point symbolic link to the list of iSCSI persistently bound volumes and devices.




## -parameters




### -param DevicePath [in]

A drive letter or symbolic link for a mount point of the volume.


## -returns



Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns one of the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ISDSC_DEVICE_NOT_ISCSI_OR_PERSISTENT</b></dt>
</dl>
</td>
<td width="60%">
The volume or device is not located on a iSCSI target or the session to the iSCSI target is not persistent. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ISDSC_VOLUME_ALREADY_PERSISTENTLY_BOUND</b></dt>
</dl>
</td>
<td width="60%">
The volume or device is already in the persistent volume or device list. 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9e21dde6-face-40ae-803b-2aa7861e6f4f">ClearPersistentScsiDevices</a>



<a href="https://msdn.microsoft.com/2522f906-2a91-4d5b-8d6b-86e22c707046">RemoveIscsiPersistentTarget</a>



<a href="https://msdn.microsoft.com/4016d8e4-de67-4c49-b54f-31c1b7bd64a8">RemovePersistentIscsiDevice</a>



<a href="https://msdn.microsoft.com/0ab1a864-b44e-4307-9f7c-93cc0d40ff3a">ReportIscsiPersistentLogins</a>



<a href="https://msdn.microsoft.com/856e240d-8c4d-4e55-aef3-71f98193c221">ReportPersistentIscsiDevices</a>



<a href="https://msdn.microsoft.com/b21e5872-24b2-4a4c-86a7-528789c1b9aa">SetupPersistentIscsiDevices</a>
 

 

