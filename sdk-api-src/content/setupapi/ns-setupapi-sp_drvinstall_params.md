---
UID: NS:setupapi._SP_DRVINSTALL_PARAMS
title: SP_DRVINSTALL_PARAMS (setupapi.h)
description: An SP_DRVINSTALL_PARAMS structure contains driver installation parameters associated with a particular driver information element.
old-location: devinst\sp_drvinstall_params.htm
tech.root: devinst
ms.assetid: 300e636c-3f77-4d0b-9868-caaf92d87bfd
ms.date: 12/05/2018
ms.keywords: "*PSP_DRVINSTALL_PARAMS, PSP_DRVINSTALL_PARAMS, PSP_DRVINSTALL_PARAMS structure pointer [Device and Driver Installation], SP_DRVINSTALL_PARAMS, SP_DRVINSTALL_PARAMS structure [Device and Driver Installation], devinst.sp_drvinstall_params, di-struct_32ef55e7-dc77-4350-b220-6cd566cf7c38.xml, setupapi/PSP_DRVINSTALL_PARAMS, setupapi/SP_DRVINSTALL_PARAMS"
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Windows
req.target-min-winverclnt: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SP_DRVINSTALL_PARAMS, *PSP_DRVINSTALL_PARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SP_DRVINSTALL_PARAMS
 - setupapi/_SP_DRVINSTALL_PARAMS
 - PSP_DRVINSTALL_PARAMS
 - setupapi/PSP_DRVINSTALL_PARAMS
 - SP_DRVINSTALL_PARAMS
 - setupapi/SP_DRVINSTALL_PARAMS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - setupapi.h
api_name:
 - SP_DRVINSTALL_PARAMS
---

# SP_DRVINSTALL_PARAMS structure


## -description

An SP_DRVINSTALL_PARAMS structure contains driver installation parameters associated with a particular driver information element.

## -struct-fields

### -field cbSize

The size, in bytes, of the SP_DRVINSTALL_PARAMS structure.

### -field Rank

The rank match of this driver. Ranges from 0 to <i>n</i>, where 0 is the most compatible.

### -field Flags

Flags that control functions operating on this driver. Can be a combination of the following:





#### DNF_ALWAYSEXCLUDEFROMLIST (Windows Vista and later versions of Windows)

If set, this flag prevents the <a href="/windows-hardware/drivers/">driver node</a> from being enumerated, regardless of the client that is performing the enumeration.





#### DNF_AUTHENTICODE_SIGNED (Windows Server 2003 and later versions of Windows)

This driver's INF file is signed by an Authenticode signature. This flag is read-only to installers.

For more information, see <a href="/windows-hardware/drivers/install/using-setupapi-to-verify-driver-authenticode-signatures">Using SetupAPI to Verify Driver Authenticode Signatures</a>.



#### DNF_BAD_DRIVER

Do not use this driver. Installers can read and write this flag.

If this flag is set, <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiselectbestcompatdrv">SetupDiSelectBestCompatDrv</a> and <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiselectdevice">SetupDiSelectDevice</a> ignore this driver.

A class installer or co-installer can set this flag to prevent Windows from listing the driver in the Select Driver dialog box. An installer might set this flag when it handles a <a href="/windows-hardware/drivers/install/dif-selectdevice">DIF_SELECTDEVICE</a> or <a href="/windows-hardware/drivers/install/dif-selectbestcompatdrv">DIF_SELECTBESTCOMPATDRV</a> request, for example. 



#### DNF_BASIC_DRIVER (Windows XP and later versions of Windows)

This driver is a basic driver. This flag is read-only to installers.



#### DNF_CLASS_DRIVER

This driver is a class driver. This flag is read-only to installers.



#### DNF_COMPATIBLE_DRIVER

This driver is a compatible driver. This flag is read-only to installers.



#### DNF_DUPDESC

There are other providers supplying drivers that have the same description as this driver. This flag is read-only to installers.



#### DNF_DUPDRIVERVER (Windows XP and later versions of Windows)

There are other providers supplying drivers that have the same version as this driver. This flag is read-only to installers.



#### DNF_DUPPROVIDER

There are other providers supplying drivers that have the same description as this driver. The only difference between this driver and its match is the driver date. This flag is read-only to installers.

If this flag is set, Windows displays the driver date and driver version next to the driver so that the user can distinguish it from its match. 



#### DNF_EXCLUDEFROMLIST

Do not display this driver in any driver-select dialogs.



#### DNF_INBOX_DRIVER (Windows Vista and later versions of Windows)

This <a href="/windows-hardware/drivers/">driver node</a> is derived from an INF file that was included with this version of Windows.



#### DNF_INET_DRIVER

This driver came from the Internet or from Windows Update. This flag is read-only to installers. 

If you call <a href="/windows/win32/api/setupapi/nf-setupapi-setupcopyoeminfa">SetupCopyOEMInf</a> you must specify the SPOST_URL flag so that when Windows copies this INF into the %<i>SystemRoot</i>%&#92;<i>inf</i> directory Windows will mark it as an Internet INF. If you omit this step then Windows will attempt to use this device to install other devices. The resulting problem is that Windows does not have the source files any longer and will end up prompting the user with an invalid path.



#### DNF_INF_IS_SIGNED (Windows XP and later versions of Windows)

This flag is read-only to installers, and is set if any of the following conditions are true:

<ul>
<li>The driver has a <a href="/windows-hardware/drivers/install/whql-release-signature">WHQL release signature</a>.</li>
<li>The driver is an inbox driver.</li>
<li>The driver has an Authenticode signature.</li>
</ul>
For more information, see <a href="/windows-hardware/drivers/install/driver-signing">Driver Signing</a>.



#### DNF_INSTALLEDDRIVER (Windows Vista and later versions of Windows)

This <a href="/windows-hardware/drivers/">driver node</a> is currently installed for the device. This flag is read-only to installers.



#### DNF_LEGACYINF

This driver comes from a legacy INF file. This flag is valid only for the NT-based operating system. This flag is read-only to installers.



#### DNF_NODRIVER

Set if no physical driver is to be installed for this logical driver.



#### DNF_OEM_F6_INF (Windows XP and later versions of Windows)

Reserved.



#### DNF_OLD_INET_DRIVER

This driver came from the Internet, but Windows does not currently have access to its source files. This flag is read-only to installers.

The system will not install a driver marked with this flag because Windows does not have the source files and would end up prompting the user with an invalid path. The INF for such a driver can be used for everything except for installing devices.



#### DNF_OLDDRIVER

This driver currently/previously controlled the associated device. This flag is read-only to installers.



#### DNF_REQUESTADDITIONALSOFTWARE (Windows 7 and later versions of Windows)

Set this flag if the <a href="/windows-hardware/drivers/install/difx-guidelines">driver package</a> is only part of the software solution that is needed to operate the device. In this case, the driver package requires the installation of additional software.

For more information, see the following Remarks section.

### -field PrivateData

A field a class installer can use to store private data. Co-installers should not use this field.

### -field Reserved

Reserved. For internal use only.

## -remarks

Starting with Windows 7, an installer or co-installer can set the DNF_REQUESTADDITIONALSOFTWARE flag to indicate that the <a href="/windows-hardware/drivers/install/difx-guidelines">driver package</a> requires additional software that may or not be installed in the computer.

After the <a href="/windows-hardware/drivers/install/difx-guidelines">driver package</a> for the device is installed, the Plug and Play (PnP) manager performs the following steps if the installer sets the DNF_REQUESTADDITIONALSOFTWARE flag:

<ol>
<li>
The PnP manager generates a Problem Report and Solution (PRS) error report with the type of <b>RequestAddtionalSoftware</b>. This report contains information about the specific hardware ID of the device and the system architecture of the computer. 

</li>
<li>
If there is a solution that is provided by the independent hardware vendor (IHV) for the device-specific software, the solution is downloaded to the computer.

<div class="alert"><b>Note</b>  The download of the solution does not install the software itself.</div>
<div> </div>
</li>
<li>
If the device-specific software is not installed on the computer, the PnP manager presents the solution to the user and provides a link to download the software. The user can then choose to download and install this software by following the instructions presented in the solution.

</li>
</ol>
<div class="alert"><b>Note</b>  The installer does not have to set the DNF_REQUESTADDITIONALSOFTWARE flag if the INF file for the <a href="/previous-versions/windows/hardware/difxapi/driverpackagepreinstall">driver package</a> has set the <b>RequestAdditionalSoftware </b> flag in the <a href="/windows-hardware/drivers/install/inf-controlflags-section">INF ControlFlags Section</a>.</div>


## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdriverinstallparamsa">SetupDiGetDriverInstallParams</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdisetdriverinstallparamsa">SetupDiSetDriverInstallParams</a>
