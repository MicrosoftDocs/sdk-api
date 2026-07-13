---
UID: NF:iscsidsc.RemovePersistentIScsiDeviceW
title: RemovePersistentIScsiDeviceW function (iscsidsc.h)
description: RemovePersistentIscsiDevice function removes a device or volume from the list of persistently bound iSCSI volumes. (Unicode)
helpviewer_keywords: ["RemovePersistentIScsiDeviceW", "RemovePersistentIscsiDevice", "RemovePersistentIscsiDevice function [iSCSI Discovery Library API]", "RemovePersistentIscsiDeviceW", "iscsidisc.removepersistentiscsidevice", "iscsidsc/RemovePersistentIscsiDevice", "iscsidsc/RemovePersistentIscsiDeviceW"]
old-location: iscsidisc\removepersistentiscsidevice.htm
tech.root: iSCSIDisc
ms.assetid: 4016d8e4-de67-4c49-b54f-31c1b7bd64a8
ms.date: 12/05/2018
ms.keywords: RemovePersistentIScsiDeviceW, RemovePersistentIscsiDevice, RemovePersistentIscsiDevice function [iSCSI Discovery Library API], RemovePersistentIscsiDeviceA, RemovePersistentIscsiDeviceW, iscsidisc.removepersistentiscsidevice, iscsidsc/RemovePersistentIscsiDevice, iscsidsc/RemovePersistentIscsiDeviceA, iscsidsc/RemovePersistentIscsiDeviceW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RemovePersistentIScsiDeviceW
 - iscsidsc/RemovePersistentIScsiDeviceW
dev_langs:
 - c++
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

<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-addpersistentiscsidevicea">AddPersistentIscsiDevice</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-clearpersistentiscsidevices">ClearPersistentIscsiDevices</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-removeiscsipersistenttargeta">RemoveIscsiPersistentTarget</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-reportiscsipersistentloginsa">ReportIscsiPersistentLogins</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-reportpersistentiscsidevicesa">ReportPersistentIscsiDevices</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-setuppersistentiscsidevices">SetupPersistentIscsiDevices</a>

## -remarks

> [!NOTE]
> The iscsidsc.h header defines RemovePersistentIScsiDevice as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
