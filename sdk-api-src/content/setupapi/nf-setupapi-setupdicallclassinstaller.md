---
UID: NF:setupapi.SetupDiCallClassInstaller
title: SetupDiCallClassInstaller function (setupapi.h)
description: The SetupDiCallClassInstaller function calls the appropriate class installer, and any registered co-installers, with the specified installation request (DIF code).
helpviewer_keywords: ["SetupDiCallClassInstaller","SetupDiCallClassInstaller function [Device and Driver Installation]","devinst.setupdicallclassinstaller","di-rtns_eff914b0-a2db-4eb5-a9b8-f2990efcf252.xml","setupapi/SetupDiCallClassInstaller"]
old-location: devinst\setupdicallclassinstaller.htm
tech.root: devinst
ms.assetid: 2aa631c3-8d00-4309-a37c-efaa7eda3efa
ms.date: 12/05/2018
ms.keywords: SetupDiCallClassInstaller, SetupDiCallClassInstaller function [Device and Driver Installation], devinst.setupdicallclassinstaller, di-rtns_eff914b0-a2db-4eb5-a9b8-f2990efcf252.xml, setupapi/SetupDiCallClassInstaller
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
 - SetupDiCallClassInstaller
 - setupapi/SetupDiCallClassInstaller
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
 - Ext-MS-Win-SetupAPI-ClassInstallers-l1-1-0.dll
 - Ext-MS-Win-SetupAPI-ClassInstallers-l1-1-1.dll
 - Ext-MS-Win-SetupAPI-ClassInstallers-L1-1-2.dll
api_name:
 - SetupDiCallClassInstaller
req.apiset: ext-ms-win-setupapi-classinstallers-l1-1-0 (introduced in Windows 8)
---

# SetupDiCallClassInstaller function


## -description

The <b>SetupDiCallClassInstaller</b> function calls the appropriate class installer, and any registered co-installers, with the specified installation request (DIF code).

## -parameters

### -param InstallFunction [in]

The device installation request (DIF request) to pass to the co-installers and class installer. DIF codes have the format <b>DIF_<i>XXX</i></b> and are defined in Setupapi.h. See <a href="/windows-hardware/drivers/install/handling-dif-codes">Device Installation Function Codes</a> for more information.

<div class="alert"><b>Note</b>  For certain DIF requests, the caller must be a member of the Administrators group. For such DIF requests, this requirement is listed on the reference page for the associated default handler.</div>
<div> </div>

### -param DeviceInfoSet [in]

A handle to a <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> for the local computer. This set contains a device installation element which represents the device for which to perform the specified installation function.

### -param DeviceInfoData [in, optional]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that specifies the device information element in the <i>DeviceInfoSet</i> that represents the device for which to perform the specified installation function. This parameter is optional and can be set to <b>NULL</b>. If this parameter is specified, <b>SetupDiCallClassInstaller</b> performs the specified function on the <i>DeviceInfoData</i> element. If <i>DeviceInfoData</i> is <b>NULL</b>, <b>SetupDiCallClassInstaller</b> calls the installers for the setup class that is associated with <i>DeviceInfoSet</i>.

## -returns

The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by making a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.


When GetLastError returns <b>ERROR_IN_WOW64</b>, this means that the calling application is a 32-bit application attempting to execute in a 64-bit environment, which is not allowed.

## -remarks

<b>SetupDiCallClassInstaller</b> calls the class installer and any co-installers that are registered for a device or a <a href="/windows-hardware/drivers/install/overview-of-device-setup-classes">device setup class</a>. This function loads the installers if they are not yet loaded. The function also calls the default handler for the DIF request, if there is a default handler and if the installers return a status indicating that the default handler should be called.

<a href="/windows-hardware/drivers/">Device installation applications</a> call this function with a variety of <a href="/windows-hardware/drivers/install/handling-dif-codes">device installation function codes</a> (DIF codes). The function ensures that all the appropriate installers and default handlers are called, in the correct order, for a given DIF request. For more information, see <a href="/windows-hardware/drivers/install/handling-dif-codes">Handling DIF Codes</a>.

After <b>SetupDiCallClassInstaller</b> returns <b>TRUE</b>, the device installation application must call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdeviceinstallparamsa">SetupDiGetDeviceInstallParams</a> to obtain an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinstall_params_a">SP_DEVINSTALL_PARAMS</a> structure. If the structure's <b>DI_NEEDREBOOT</b> or <b>DI_NEEDRESTART</b> flag is set, the caller must prompt the user to restart the system. For example, the caller can do this by calling <a href="/windows/desktop/api/setupapi/nf-setupapi-setuppromptreboot">SetupPromptReboot</a>. 

However, be aware that a device installation application should request a system restart one time at most. Therefore, any device installation application that creates multiple calls to <b>SetupDiCallClassInstaller</b> and <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdeviceinstallparamsa">SetupDiGetDeviceInstallParams</a> should save the <b>DI_NEEDREBOOT</b> and <b>DI_NEEDRESTART</b> flags after each call. However, it should prompt the user only after the last call returns. 

In response to a DIF code supplied by <b>SetupDiCallClassInstaller</b>, class installers and co-installers might perform operations that require the system to be restarted. In such situations, the installer or co-installer should do the following: 

<ol>
<li>
Call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdeviceinstallparamsa">SetupDiGetDeviceInstallParams</a> to obtain the <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinstall_params_a">SP_DEVINSTALL_PARAMS</a> structure. 

</li>
<li>
Set the <b>DI_NEEDREBOOT</b> or <b>DI_NEEDRESTART</b> flag in the structure's <i>Flags</i> member.

</li>
<li>
Call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdisetdeviceinstallparamsa">SetupDiSetDeviceInstallParams</a>, supplying the updated <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinstall_params_a">SP_DEVINSTALL_PARAMS</a> structure, to save the revised <i>Flags</i> member.

</li>
</ol>
After <b>SetupDiCallClassInstaller</b> returns, the device installation application that called it should call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdeviceinstallparamsa">SetupDiGetDeviceInstallParams</a>, check the flags, and request a restart if necessary.

The device information set specified by <i>DeviceInfoSet</i> must only contain elements for devices on the local computer.

For information about the design and operation of co-installers, see <a href="/windows-hardware/drivers/install/writing-a-co-installer">Writing a Co-installer</a>.

## -see-also

<a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a>
