---
UID: NF:setupapi.SetupDiAskForOEMDisk
title: SetupDiAskForOEMDisk function (setupapi.h)
description: The SetupDiAskForOEMDisk function displays a dialog that asks the user for the path of an OEM installation disk.
helpviewer_keywords: ["SetupDiAskForOEMDisk","SetupDiAskForOEMDisk function [Device and Driver Installation]","devinst.setupdiaskforoemdisk","di-rtns_4b903984-cb48-48d3-9de8-dc68a79128c2.xml","setupapi/SetupDiAskForOEMDisk"]
old-location: devinst\setupdiaskforoemdisk.htm
tech.root: devinst
ms.assetid: 5be03143-3de0-43ed-a027-832f1e275527
ms.date: 12/05/2018
ms.keywords: SetupDiAskForOEMDisk, SetupDiAskForOEMDisk function [Device and Driver Installation], devinst.setupdiaskforoemdisk, di-rtns_4b903984-cb48-48d3-9de8-dc68a79128c2.xml, setupapi/SetupDiAskForOEMDisk
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
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
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupDiAskForOEMDisk
 - setupapi/SetupDiAskForOEMDisk
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
api_name:
 - SetupDiAskForOEMDisk
---

# SetupDiAskForOEMDisk function


## -description

The <b>SetupDiAskForOEMDisk</b> function displays a dialog that asks the user for the path of an OEM installation disk.

## -parameters

### -param DeviceInfoSet [in]

A handle to a <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> for the local computer. This set contains a device information element that represents the device that is being installed.

### -param DeviceInfoData [in, optional]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>. This parameter is optional and can be <b>NULL</b>. If this parameter is specified, <b>SetupDiAskForOEMDisk</b> associates the driver with the device that is being installed. If this parameter is <b>NULL</b>, <b>SetupDiAskForOEMDisk</b> associates the driver with the global class driver list for <i>DeviceInfoSet</i>.

## -returns

The function returns <b>TRUE</b> if it is successful and the <b>DriverPath</b> field of the SP_DEVINSTALLPARAMS structure is updated to reflect the new path. If the user cancels the dialog, the function returns <b>FALSE</b> and a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_CANCELLED.

## -remarks

<b>SetupDiAskForOEMDisk</b> allows the user to browse local and network drives for OEM installation files. However, <b>SetupDiAskForOEMDisk</b> is primarily designed to obtain the path of an OEM driver on a local computer before selecting and installing the driver for a device on that computer.

Although this function will not fail if the device information set if for a remote computer, the result is of limited use because the device information set cannot subsequently be used with DIF_<i>Xxx</i> installation requests or <b>SetupDi</b><i>Xxx</i> functions that do not support operations on a remote computer.

In particular, the device information set cannot be used as input with a DIF_SELECTDEVICE installation request to select a driver for a device, followed by a DIF_INSTALLDEVICE installation request to install a device on a remote computer.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiselectoemdrv">SetupDiSelectOEMDrv</a>