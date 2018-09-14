---
UID: NF:iscsidsc.RemovePersistentIScsiDeviceW
title: RemovePersistentIScsiDeviceW function
author: windows-sdk-content
description: RemovePersistentIscsiDevice function removes a device or volume from the list of persistently bound iSCSI volumes.
old-location: iscsidisc\removepersistentiscsidevice.htm
tech.root: iSCSIDisc
ms.assetid: 4016d8e4-de67-4c49-b54f-31c1b7bd64a8
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: RemovePersistentIScsiDeviceW, RemovePersistentIscsiDevice, RemovePersistentIscsiDevice function [iSCSI Discovery Library API], RemovePersistentIscsiDeviceA, RemovePersistentIscsiDeviceW, iscsidisc.removepersistentiscsidevice, iscsidsc/RemovePersistentIscsiDevice, iscsidsc/RemovePersistentIscsiDeviceA, iscsidsc/RemovePersistentIscsiDeviceW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RemovePersistentIscsiDeviceW (Unicode) and RemovePersistentIscsiDeviceA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Iscsidsc.lib
req.dll: Iscsidsc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iscsidsc.dll
api_name:
 - RemovePersistentIscsiDevice
 - RemovePersistentIscsiDeviceA
 - RemovePersistentIscsiDeviceW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RemovePersistentIScsiDeviceW function


## -description


The <b>RemovePersistentIscsiDevice</b> function removes a device or volume from the list of persistently bound iSCSI volumes.


## -parameters




### -param DevicePath [in]

A drive letter, mount point, or device path for the volume or device.


## -returns



Returns ERROR_SUCCESS if the operation succeeds and ISDSC_DEVICE_NOT_FOUND if the volume that is specified by <i>VolumePath</i> is not in the list of persistently bound volumes. 

Otherwise, <b>RemovePersistentIscsiDevice</b> returns the appropriate Win32 or iSCSI error code on failure.




## -see-also




<a href="https://msdn.microsoft.com/184b256b-0cb0-45c1-8f73-5ff28fb388fb">AddPersistentIscsiDevice</a>



<a href="https://msdn.microsoft.com/9e21dde6-face-40ae-803b-2aa7861e6f4f">ClearPersistentIscsiDevices</a>



<a href="https://msdn.microsoft.com/2522f906-2a91-4d5b-8d6b-86e22c707046">RemoveIscsiPersistentTarget</a>



<a href="https://msdn.microsoft.com/0ab1a864-b44e-4307-9f7c-93cc0d40ff3a">ReportIscsiPersistentLogins</a>



<a href="https://msdn.microsoft.com/856e240d-8c4d-4e55-aef3-71f98193c221">ReportPersistentIscsiDevices</a>



<a href="https://msdn.microsoft.com/b21e5872-24b2-4a4c-86a7-528789c1b9aa">SetupPersistentIscsiDevices</a>
 

 

