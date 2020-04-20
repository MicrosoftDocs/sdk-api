---
UID: NF:iscsidsc.RemovePersistentIScsiDeviceA
title: RemovePersistentIScsiDeviceA function (iscsidsc.h)
description: RemovePersistentIscsiDevice function removes a device or volume from the list of persistently bound iSCSI volumes.helpviewer_keywords: ["RemovePersistentIScsiDeviceA","RemovePersistentIscsiDevice","RemovePersistentIscsiDevice function [iSCSI Discovery Library API]","RemovePersistentIscsiDeviceA","RemovePersistentIscsiDeviceW","iscsidisc.removepersistentiscsidevice","iscsidsc/RemovePersistentIscsiDevice","iscsidsc/RemovePersistentIscsiDeviceA","iscsidsc/RemovePersistentIscsiDeviceW"]
old-location: iscsidisc\removepersistentiscsidevice.htm
tech.root: iSCSIDisc
ms.assetid: 4016d8e4-de67-4c49-b54f-31c1b7bd64a8
ms.date: 12/05/2018
ms.keywords: RemovePersistentIScsiDeviceA, RemovePersistentIscsiDevice, RemovePersistentIscsiDevice function [iSCSI Discovery Library API], RemovePersistentIscsiDeviceA, RemovePersistentIscsiDeviceW, iscsidisc.removepersistentiscsidevice, iscsidsc/RemovePersistentIscsiDevice, iscsidsc/RemovePersistentIscsiDeviceA, iscsidsc/RemovePersistentIscsiDeviceW
f1_keywords:
- iscsidsc/RemovePersistentIscsiDevice
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RemovePersistentIScsiDeviceA function


## -description


The <b>RemovePersistentIscsiDevice</b> function removes a device or volume from the list of persistently bound iSCSI volumes.


## -parameters




### -param DevicePath [in]

A drive letter, mount point, or device path for the volume or device.


## -returns



Returns ERROR_SUCCESS if the operation succeeds and ISDSC_DEVICE_NOT_FOUND if the volume that is specified by <i>VolumePath</i> is not in the list of persistently bound volumes. 

Otherwise, <b>RemovePersistentIscsiDevice</b> returns the appropriate Win32 or iSCSI error code on failure.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-addpersistentiscsidevicea">AddPersistentIscsiDevice</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-clearpersistentiscsidevices">ClearPersistentIscsiDevices</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-removeiscsipersistenttargeta">RemoveIscsiPersistentTarget</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-reportiscsipersistentloginsa">ReportIscsiPersistentLogins</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-reportpersistentiscsidevicesa">ReportPersistentIscsiDevices</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-setuppersistentiscsidevices">SetupPersistentIscsiDevices</a>
 

 

