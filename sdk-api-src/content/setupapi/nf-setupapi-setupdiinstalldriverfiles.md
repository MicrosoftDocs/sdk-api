---
UID: NF:setupapi.SetupDiInstallDriverFiles
title: SetupDiInstallDriverFiles function (setupapi.h)
description: The SetupDiInstallDriverFiles function is the default handler for the DIF_INSTALLDEVICEFILES installation request.
helpviewer_keywords: ["SetupDiInstallDriverFiles","SetupDiInstallDriverFiles function [Device and Driver Installation]","devinst.setupdiinstalldriverfiles","di-rtns_0790674a-71fa-469e-b716-d420fbf40e7b.xml","setupapi/SetupDiInstallDriverFiles"]
old-location: devinst\setupdiinstalldriverfiles.htm
tech.root: devinst
ms.assetid: 55abcdd1-a33e-4100-a3dd-4d3a31158004
ms.date: 12/05/2018
ms.keywords: SetupDiInstallDriverFiles, SetupDiInstallDriverFiles function [Device and Driver Installation], devinst.setupdiinstalldriverfiles, di-rtns_0790674a-71fa-469e-b716-d420fbf40e7b.xml, setupapi/SetupDiInstallDriverFiles
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
 - SetupDiInstallDriverFiles
 - setupapi/SetupDiInstallDriverFiles
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
 - SetupDiInstallDriverFiles
---

# SetupDiInstallDriverFiles function


## -description

The <b>SetupDiInstallDriverFiles</b> function is the default handler for the <a href="/windows-hardware/drivers/install/dif-installdevicefiles">DIF_INSTALLDEVICEFILES</a> installation request.

## -parameters

### -param DeviceInfoSet [in]

A handle to the <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains the device information element that represents the device for which to install files. The device information set must not contain remote elements.

### -param DeviceInfoData [in]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>.

## -returns

The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The caller of <b>SetupDiInstallDriverFiles</b> must be a member of the Administrators group if this function is being used to install files. However, if this function is being used to build up a file queue, membership in the Administrators group is not required.

<div class="alert"><b>Note</b>  Only a class installer should call <b>SetupDiInstallDriverFiles</b> and only in those situations where the class installer must perform driver file installation operations after <b>SetupDiInstallDriverFiles</b> completes the default driver file installation operation. In such situations, the class installer must directly call <b>SetupDiInstallDriverFiles</b> when the installer processes a DIF_INSTALLDEVICEFILES request. For more information about calling the default handler, see <a href="/windows-hardware/drivers/install/calling-the-default-dif-code-handlers">Calling Default DIF Code Handlers</a>.</div>
<div> </div>
The operation of <b>SetupDiInstallDriverFiles</b> is similar to the <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiinstalldevice">SetupDiInstallDevice</a> function. However, this function performs only the file copy operations that are performed by <b>SetupDiInstallDevice</b>. 

A driver must be selected for the specified device information set or element before this function is called.

This function processes the <b>CopyFiles</b>, <b>Delfiles</b>, and <b>Renfiles</b> entries in the selected INF file.

The <i>DeviceInfoSet</i> must only contain elements on the local computer.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicallclassinstaller">SetupDiCallClassInstaller</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiinstalldevice">SetupDiInstallDevice</a>