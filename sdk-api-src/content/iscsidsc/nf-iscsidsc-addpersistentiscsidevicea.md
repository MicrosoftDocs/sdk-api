---
UID: NF:iscsidsc.AddPersistentIScsiDeviceA
title: AddPersistentIScsiDeviceA function (iscsidsc.h)
description: AddPersistentIscsiDevice function adds a volume device name, drive letter, or mount point symbolic link to the list of iSCSI persistently bound volumes and devices. (ANSI)
helpviewer_keywords: ["AddPersistentIScsiDeviceA", "AddPersistentIscsiDeviceA", "iscsidsc/AddPersistentIscsiDeviceA"]
old-location: iscsidisc\addpersistentiscsidevice.htm
tech.root: iSCSIDisc
ms.assetid: 184b256b-0cb0-45c1-8f73-5ff28fb388fb
ms.date: 12/05/2018
ms.keywords: AddPersistentIScsiDeviceA, AddPersistentIscsiDevice, AddPersistentIscsiDevice function [iSCSI Discovery Library API], AddPersistentIscsiDeviceA, AddPersistentIscsiDeviceW, AddPersistentiScsiDevice, iscsidisc.addpersistentiscsidevice, iscsidsc/AddPersistentIscsiDevice, iscsidsc/AddPersistentIscsiDeviceA, iscsidsc/AddPersistentIscsiDeviceW
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
req.lib: Iscsidsc.lib
req.dll: Iscsidsc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AddPersistentIScsiDeviceA
 - iscsidsc/AddPersistentIScsiDeviceA
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
 - AddPersistentIscsiDevice
 - AddPersistentIscsiDeviceA
 - AddPersistentIscsiDeviceW
---

# AddPersistentIScsiDeviceA function


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

<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-clearpersistentiscsidevices">ClearPersistentScsiDevices</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-removeiscsipersistenttargeta">RemoveIscsiPersistentTarget</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-removepersistentiscsidevicea">RemovePersistentIscsiDevice</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-reportiscsipersistentloginsa">ReportIscsiPersistentLogins</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-reportpersistentiscsidevicesa">ReportPersistentIscsiDevices</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-setuppersistentiscsidevices">SetupPersistentIscsiDevices</a>

## -remarks

> [!NOTE]
> The iscsidsc.h header defines AddPersistentIScsiDevice as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
