---
UID: NF:setupapi.SetupDiInstallDeviceInterfaces
title: SetupDiInstallDeviceInterfaces function (setupapi.h)
description: The SetupDiInstallDeviceInterfaces function is the default handler for the DIF_INSTALLINTERFACES installation request.
helpviewer_keywords: ["SetupDiInstallDeviceInterfaces","SetupDiInstallDeviceInterfaces function [Device and Driver Installation]","devinst.setupdiinstalldeviceinterfaces","di-rtns_8bb9c70f-c1be-45f6-af6c-243a750babb9.xml","setupapi/SetupDiInstallDeviceInterfaces"]
old-location: devinst\setupdiinstalldeviceinterfaces.htm
tech.root: devinst
ms.assetid: c47d83f6-9ae5-43a9-a6ed-b0441b490e8d
ms.date: 12/05/2018
ms.keywords: SetupDiInstallDeviceInterfaces, SetupDiInstallDeviceInterfaces function [Device and Driver Installation], devinst.setupdiinstalldeviceinterfaces, di-rtns_8bb9c70f-c1be-45f6-af6c-243a750babb9.xml, setupapi/SetupDiInstallDeviceInterfaces
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
 - SetupDiInstallDeviceInterfaces
 - setupapi/SetupDiInstallDeviceInterfaces
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
 - SetupDiInstallDeviceInterfaces
---

# SetupDiInstallDeviceInterfaces function


## -description

The <b>SetupDiInstallDeviceInterfaces</b> function is the default handler for the <a href="/windows-hardware/drivers/install/dif-installinterfaces">DIF_INSTALLINTERFACES</a> installation request.

## -parameters

### -param DeviceInfoSet [in]

A pointer to the <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains a device information element that represents the device for which to install interfaces. The device information set must contain only elements for the local system.

### -param DeviceInfoData [in]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>.

## -returns

<b>SetupDiInstallDeviceInterfaces</b> returns <b>TRUE</b> if the function completed without error. If the function completed with an error, <b>FALSE</b> is returned and the error code for the failure can be retrieved by calling <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>SetupDiInstallDeviceInterfaces</b> processes each <b>AddInterface</b> entry in the <i>DDInstall</i>.<b>Interfaces</b> section of a device INF file and creates each interface by calling <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicreatedeviceinterfacea">SetupDiCreateDeviceInterface</a>.

The caller of <b>SetupDiInstallDeviceInterfaces</b> must be a member of the Administrators group. 

<div class="alert"><b>Note</b>  Only a <a href="/windows-hardware/drivers/">class installer</a> should call <b>SetupDiInstallDeviceInterfaces</b> and only in those situations where the class installer must perform device interface installation operations after <b>SetupDiInstallDeviceInterfaces</b> completes the default device interface installation operation. In such situations, the class installer must directly call <b>SetupDiInstallDeviceInterfaces</b> when the installer processes a DIF_INSTALLINTERFACES request. For more information about calling the default handler, see <a href="/windows-hardware/drivers/install/calling-the-default-dif-code-handlers">Calling Default DIF Code Handlers</a>.</div>
<div> </div>
For information about INF file format, see <a href="/windows-hardware/drivers/install/inf-file-sections-and-directives">INF File Sections and Directives</a>.

## -see-also

<a href="/windows-hardware/drivers/install/dif-installinterfaces">DIF_INSTALLINTERFACES</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicreatedeviceinterfacea">SetupDiCreateDeviceInterface</a>