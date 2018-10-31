---
UID: NS:setupapi._SP_DEVINSTALL_PARAMS_W
title: "_SP_DEVINSTALL_PARAMS_W"
author: windows-sdk-content
description: An SP_DEVINSTALL_PARAMS structure contains device installation parameters associated with a particular device information element or associated globally with a device information set.
old-location: devinst\sp_devinstall_params.htm
tech.root: devinst
ms.assetid: 1bd21150-f8f4-480d-a4b2-99fa4b4233b9
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*PSP_DEVINSTALL_PARAMS_W, PSP_DEVINSTALL_PARAMS, PSP_DEVINSTALL_PARAMS structure pointer [Device and Driver Installation], SP_DEVINSTALL_PARAMS, SP_DEVINSTALL_PARAMS structure [Device and Driver Installation], SP_DEVINSTALL_PARAMS_W, _SP_DEVINSTALL_PARAMS_W, devinst.sp_devinstall_params, di-struct_ef7906d1-6416-41fc-8844-53f2f594a913.xml, setupapi/PSP_DEVINSTALL_PARAMS, setupapi/SP_DEVINSTALL_PARAMS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - setupapi.h
api_name:
 - SP_DEVINSTALL_PARAMS
product: Windows
targetos: Windows
req.typenames: SP_DEVINSTALL_PARAMS_W, *PSP_DEVINSTALL_PARAMS_W
req.redist: 
---

# _SP_DEVINSTALL_PARAMS_W structure


## -description


An SP_DEVINSTALL_PARAMS structure contains device installation parameters associated with a particular device information element or associated globally with a device information set.


## -struct-fields




### -field cbSize

The size, in bytes, of the SP_DEVINSTALL_PARAMS structure.


### -field Flags

Flags that control installation and user interface operations. Some flags can be set before sending the device installation request while other flags are set automatically during the processing of some requests. <b>Flags</b> can be a combination of the following values. 

The flag values are listed in groups: writable by <a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">device installation applications</a> and installers, read-only (only set by the OS), reserved, and obsolete. The first group lists flags that are writable:





#### DI_CLASSINSTALLPARAMS

Set to use the Class Install parameters. <a href="https://msdn.microsoft.com/a7f35e32-eaad-440b-8109-7320048ec7ba">SetupDiSetClassInstallParams</a> sets this flag when the caller specifies parameters and clears the flag when the caller specifies a <b>NULL</b> parameters pointer. 



#### DI_COMPAT_FROM_CLASS

Set to force <a href="https://msdn.microsoft.com/9e377865-8029-41c1-85b9-fdb2cbc09346">SetupDiBuildDriverInfoList</a> to build a device's list of compatible drivers from its class driver list instead of the INF file.



#### DI_DRIVERPAGE_ADDED

Set by a class installer or co-installer if the installer supplies a page that replaces the system-supplied driver properties page. If this flag is set, the operating system does not display the system-supplied driver page.



#### DI_DONOTCALLCONFIGMG

Set if the configuration manager should not be called to remove or reenumerate devices during the execution of certain device installation functions (for example, <a href="https://msdn.microsoft.com/130a58a8-7964-40cb-87e8-4765178bd1ff">SetupDiInstallDevice</a>).

If this flag is set, device installation applications, class installers, and co-installers must not call the following functions:

<a href="https://msdn.microsoft.com/dcba5021-7517-4922-9c50-ebfa7375e258">CM_Reenumerate_DevNode</a>
<a href="https://msdn.microsoft.com/1d927aec-db3c-403f-9952-1bcc931984bf">CM_Reenumerate_DevNode_Ex</a>
<a href="https://msdn.microsoft.com/0a80cddd-d5be-42cb-ba11-0a3292b973a3">CM_Query_And_Remove_SubTree</a>
<a href="https://msdn.microsoft.com/c8a3af37-0886-4187-9cdb-49616bcb04a9">CM_Query_And_Remove_SubTree_Ex</a>
<a href="https://msdn.microsoft.com/94d0023d-d93f-42da-b2fc-54b9d8831b9b">CM_Setup_DevNode</a>
<a href="https://msdn.microsoft.com/831fdc18-1d5e-4358-8f64-59abb5e7c0e6">CM_Setup_DevNode_Ex</a>
<a href="https://msdn.microsoft.com/52c3b9b8-6d0d-4b4d-9be4-5bd0d864d2fd">CM_Set_HW_Prof_Flags</a>
<a href="https://msdn.microsoft.com/8e29d4d8-38a4-4656-b164-e214b0fc8b7d">CM_Set_HW_Prof_Flags_Ex</a>
<a href="https://msdn.microsoft.com/ddc3a507-03ee-4f44-89e3-64ec4290d0ff">CM_Enable_DevNode</a>
<a href="https://msdn.microsoft.com/582e7cdf-2302-4c9a-8834-5eada8f142d8">CM_Enable_DevNode_Ex</a>
<a href="https://msdn.microsoft.com/6013fec3-1fb3-4956-982d-5841518f5d31">CM_Disable_DevNode</a>
<a href="https://msdn.microsoft.com/d493399a-b9f7-44cc-9c0e-150137d468c8">CM_Disable_DevNode_Ex</a>


#### DI_ENUMSINGLEINF

Set if installers and other <a href="devinst.device_installation_components">device installation components</a> should only search the INF file specified by SP_DEVINSTALL_PARAMS.<b>DriverPath</b>. If this flag is set, <b>DriverPath</b> contains the path of a single INF file instead of a path of a directory.



#### DI_INF_IS_SORTED

Set to indicate that the Select Device page should list drivers in the order in which they appear in the INF file, instead of sorting them alphabetically. 



#### DI_INSTALLDISABLED

Set if the device should be installed in a disabled state by default. To be recognized, this flag must be set before Windows calls the default handler for the <a href="https://msdn.microsoft.com/2d369086-c2b6-45a4-a87e-51ff5725938f">DIF_INSTALLDEVICE</a> request. 



#### DI_NEEDREBOOT

For NT-based operating systems, this flag is set if the device requires that the computer be restarted after device installation or a device state change. A class installer or co-installer can set this flag at any time during device installation, if the installer determines that a restart is necessary.



#### DI_NEEDRESTART

The same as DI_NEEDREBOOT.



#### DI_NOBROWSE

Set to disable browsing when the user is selecting an OEM disk path. A device installation application sets this flag to constrain a user to only installing from the installation media location.



#### DI_NODI_DEFAULTACTION

Set if <a href="https://msdn.microsoft.com/2aa631c3-8d00-4309-a37c-efaa7eda3efa">SetupDiCallClassInstaller</a> should not perform any default action if the class installer returns ERR_DI_DO_DEFAULT or there is not a class installer.



#### DI_NOFILECOPY

Set if device installation applications and components, such as <a href="https://msdn.microsoft.com/130a58a8-7964-40cb-87e8-4765178bd1ff">SetupDiInstallDevice</a>, should skip file copying.



#### DI_NOVCP

Set to disable creation of a new copy queue. Use the caller-supplied copy queue in SP_DEVINSTALL_PARAMS.<b>FileQueue</b>.



#### DI_NOWRITE_IDS

Set to prevent <a href="https://msdn.microsoft.com/130a58a8-7964-40cb-87e8-4765178bd1ff">SetupDiInstallDevice</a> from writing the INF-specified <a href="devinst.hardware_ids">hardware IDs</a> and <a href="devinst.compatible_ids">compatible IDs</a> to the device properties for the device node (<a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">devnode</a>). This flag should only be set for root-enumerated devices. 

This flag overrides the DI_FLAGSEX_ALWAYSWRITEIDS flag.



#### DI_PROPERTIES_CHANGE

Set by Device Manager if a device's properties were changed, which requires an update of the installer's user interface. 



#### DI_QUIETINSTALL

Set if the device installer functions must be silent and use default choices wherever possible. Class installers and co-installers must not display any UI if this flag is set.



#### DI_RESOURCEPAGE_ADDED

Set by a class installer or co-installer if the installer supplies a page that replaces the system-supplied resource properties page. If this flag is set, the operating system does not display the system-supplied resource page.



#### DI_SHOWOEM

Set to allow support for OEM disks. If this flag is set, the operating system presents a "Have Disk" button on the Select Device page. This flag is set, by default, in system-supplied wizards.



#### DI_USECI_SELECTSTRINGS

Set if a class installer or co-installer supplied strings that should be used during <a href="https://msdn.microsoft.com/c6a512ad-bcc6-4dc5-873e-33bdaab129e2">SetupDiSelectDevice</a>.

The following flags are read-only (only set by the OS):





#### DI_DIDCLASS

Set if <a href="https://msdn.microsoft.com/9e377865-8029-41c1-85b9-fdb2cbc09346">SetupDiBuildDriverInfoList</a> has already built a list of the drivers for this class of device. If this list has already been built, it contains all the driver information and this flag is always set. <a href="https://msdn.microsoft.com/d8067609-1046-4641-9f57-b0ee2be5a3b2">SetupDiDestroyDriverInfoList</a> clears this flag when it deletes a list of drivers for a class.

This flag is read-only. Only the operating system sets this flag.



#### DI_DIDCOMPAT

Set if <a href="https://msdn.microsoft.com/9e377865-8029-41c1-85b9-fdb2cbc09346">SetupDiBuildDriverInfoList</a> has already built a list of compatible drivers for this device. If this list has already been built, it contains all the driver information and this flag is always set. <a href="https://msdn.microsoft.com/d8067609-1046-4641-9f57-b0ee2be5a3b2">SetupDiDestroyDriverInfoList</a> clears this flag when it deletes a compatible driver list.

This flag is only set in device installation parameters that are associated with a particular device information element, not in parameters for a device information set as a whole.

This flag is read-only. Only the operating system sets this flag.



#### DI_MULTMFGS

Set by <a href="https://msdn.microsoft.com/9e377865-8029-41c1-85b9-fdb2cbc09346">SetupDiBuildDriverInfoList</a> if a list of drivers for a <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff552344">device setup class</a> contains drivers that are provided by multiple manufacturers.

This flag is read-only. Only the operating system sets this flag.

The following flags are reserved:

DI_AUTOASSIGNRES 

DI_DISABLED 

DI_FORCECOPY 

DI_GENERALPAGE_ADDED 

DI_OVERRIDE_INFFLAGS 

DI_SHOWALL 

DI_SHOWCLASS 

DI_SHOWCOMPAT 

The following flags are obsolete:

DI_NOSELECTICONS 

DI_PROPS_NOCHANGEUSAGE 


### -field FlagsEx

Additional flags that provide control over installation and user interface operations. Some flags can be set before calling the device installer functions while other flags are set automatically during the processing of some functions. <b>FlagsEx</b> can be a combination of the following values.

The flag values are listed in groups: writable by device installation applications and installers, read-only (only set by the OS), reserved, and obsolete. 

The first group lists flags that are writable:





#### DI_FLAGSEX_ALLOWEXCLUDEDDRVS

If set, include drivers that were marked "Exclude From Select." 

For example, if this flag is set, <a href="https://msdn.microsoft.com/c6a512ad-bcc6-4dc5-873e-33bdaab129e2">SetupDiSelectDevice</a> displays drivers that have the Exclude From Select state and <a href="https://msdn.microsoft.com/9e377865-8029-41c1-85b9-fdb2cbc09346">SetupDiBuildDriverInfoList</a> includes Exclude From Select drivers in the requested driver list. 

A driver is "Exclude From Select" if either it is marked <b>ExcludeFromSelect</b> in the INF file or it is a driver for a device whose whole setup class is marked <b>NoInstallClass</b> or <b>NoUseClass</b> in the class installer INF. Drivers for PnP devices are typically "Exclude From Select"; PnP devices should not be manually installed. To build a list of driver files for a PnP device a caller of <b>SetupDiBuildDriverInfoList</b> must set this flag. 



#### DI_FLAGSEX_ALWAYSWRITEIDS

If set and the DI_NOWRITE_IDS flag is clear, always write hardware and compatible IDs to the device properties for the devnode. This flag should only be set for root-enumerated devices.



#### DI_FLAGSEX_APPENDDRIVERLIST

If set, <b>SetupDiBuildDriverInfoList</b> appends a new driver list to an existing list. This flag is relevant when searching multiple locations.



#### DI_FLAGSEX_DRIVERLIST_FROM_URL

If set, build the driver list from INF(s) retrieved from the URL that is specified in SP_DEVINSTALL_PARAMS.<b>DriverPath</b>. If the <b>DriverPath</b> is an empty string, use the Windows Update website.

Currently, the operating system does not support URLs. Use this flag to direct <b>SetupDiBuildDriverInfoList</b> to search the Windows Update website.

Do not set this flag if DI_QUIETINSTALL is set.



#### DI_FLAGSEX_EXCLUDE_OLD_INET_DRIVERS

If set, do not include old Internet drivers when building a driver list. This flag should be set any time that you are building a list of potential drivers for a device. You can clear this flag if you are just getting a list of drivers currently installed for a device. 



#### DI_FLAGSEX_FILTERCLASSES

If set, <a href="https://msdn.microsoft.com/a01b1f8f-55af-4053-8c31-9329ef36f2ce">SetupDiBuildClassInfoList</a> will check for class inclusion filters. This means that a device will not be included in the class list if its class is marked as NoInstallClass.



#### DI_FLAGSEX_FILTERSIMILARDRIVERS

(Windows XP and later.) If set, <a href="https://msdn.microsoft.com/9e377865-8029-41c1-85b9-fdb2cbc09346">SetupDiBuildDriverInfoList</a> includes "similar" drivers when building a class driver list. A "similar" driver is one for which one of the hardware IDs or compatible IDs in the INF file partially (or completely) matches one of the hardware IDs or compatible IDs of the hardware.



#### DI_FLAGSEX_INET_DRIVER

If set, the driver was obtained from the Internet. Windows will not use the device's INF to install future devices because Windows cannot guarantee that it can retrieve the driver files again from the Internet.



#### DI_FLAGSEX_INSTALLEDDRIVER

(Windows XP and later.) If set, <a href="https://msdn.microsoft.com/9e377865-8029-41c1-85b9-fdb2cbc09346">SetupDiBuildDriverInfoList</a> includes only the currently installed driver when creating a list of class drivers or device-compatible drivers.



#### DI_FLAGSEX_NO_DRVREG_MODIFY

Do not process the <b>AddReg</b> and <b>DelReg</b> entries for the device's hardware and software (driver) keys. That is, the <b>AddReg</b> and <b>DelReg</b> entries in the INF file <i>DDInstall</i> and <i>DDInstall</i><b>.HW</b> sections.



#### DI_FLAGSEX_POWERPAGE_ADDED

If set, an installer added their own page for the power properties dialog. The operating system will not display the system-supplied power properties page. This flag is only relevant if the device supports power management.



#### DI_FLAGSEX_PROPCHANGE_PENDING

If set, the user made changes to one or more device property sheets. The property-page provider typically sets this flag.

When the user closes the device property sheet, Device Manager checks the DI_FLAGSEX_PROPCHANGE_PENDING flag. If it is set, Device Manager clears this flag, sets the DI_PROPERTIES_CHANGE flag, and sends a DIF_PROPERTYCHANGE request to the installers to notify them that something has changed.



#### DI_FLAGSEX_SETFAILEDINSTALL

Set if the installation failed. If this flag is set, the <a href="https://msdn.microsoft.com/130a58a8-7964-40cb-87e8-4765178bd1ff">SetupDiInstallDevice</a> function just sets the FAILEDINSTALL flag in the device's <b>ConfigFlags</b> registry value. If DI_FLAGSEX_SETFAILEDINSTALL is set, co-installers must return NO_ERROR in response to DIF_INSTALLDEVICE, while class installers must return NO_ERROR or ERROR_DI_DO_DEFAULT.



#### DI_FLAGSEX_USECLASSFORCOMPAT

Filter INF files on the device's setup class when building a list of compatible drivers. If a device's setup class is known, setting this flag reduces the time that is required to build a list of compatible drivers when searching INF files that are not precompiled. This flag is ignored if DI_COMPAT_FROM_CLASS is set.

The following flags are read-only; only the operating system sets these flags:





#### DI_FLAGSEX_CI_FAILED

Set by the operating system if a class installer failed to load or start. This flag is read-only.



#### DI_FLAGSEX_DIDCOMPATINFO

Windows has built a list of <a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">driver nodes</a> that are compatible with the device. This flag is read-only.



#### DI_FLAGSEX_DIDINFOLIST

Windows has built a list of driver nodes that includes all the drivers that are listed in the INF files of the specified setup class. If the specified setup class is <b>NULL</b> because the HDEVINFO set or device has no associated class, the list includes all driver nodes from all available INF files. This flag is read-only.



#### DI_FLAGSEX_IN_SYSTEM_SETUP

If set, installation is occurring during initial system setup. This flag is read-only.

The following flags are reserved:

DI_FLAGSEX_BACKUPONREPLACE 

DI_FLAGSEX_DEVICECHANGE 

DI_FLAGSEX_OLDINF_IN_CLASSLIST 

DI_FLAGSEX_PREINSTALLBACKUP 

DI_FLAGSEX_USEOLDINFSEARCH 

The following flags are obsolete:

DI_FLAGSEX_AUTOSELECTRANK0 

DI_FLAGSEX_NOUIONQUERYREMOVE 


### -field hwndParent

Window handle that will own the user interface dialogs related to this device.


### -field InstallMsgHandler

Callback used to handle events during file copying. An installer can use a callback, for example, to perform special processing when committing a file queue.


### -field InstallMsgHandlerContext

Private data that is used by the <b>InstallMsgHandler</b> callback.


### -field FileQueue

A handle to a caller-supplied file queue where file operations should be queued but not committed.

If you associate a file queue with a device information set (<a href="https://msdn.microsoft.com/20384538-e124-41f7-94a6-c0fb9f5fe6a0">SetupDiSetDeviceInstallParams</a>), you must disassociate the queue from the device information set before you delete the device information set. If you fail to disassociate the file queue, Windows cannot decrement its reference count on the device information set and cannot free the memory.

This queue is only used if the DI_NOVCP flag is set, indicating that file operations should be enqueued but not committed.


### -field ClassInstallReserved

A pointer for class-installer data. Co-installers must not use this field. 


### -field Reserved

Reserved. For internal use only.


### -field DriverPath

This path is used by the <a href="https://msdn.microsoft.com/9e377865-8029-41c1-85b9-fdb2cbc09346">SetupDiBuildDriverInfoList</a> function. 


##### - Flags.DI_CLASSINSTALLPARAMS

Set to use the Class Install parameters. <a href="https://msdn.microsoft.com/a7f35e32-eaad-440b-8109-7320048ec7ba">SetupDiSetClassInstallParams</a> sets this flag when the caller specifies parameters and clears the flag when the caller specifies a <b>NULL</b> parameters pointer. 


##### - Flags.DI_COMPAT_FROM_CLASS

Set to force <a href="https://msdn.microsoft.com/9e377865-8029-41c1-85b9-fdb2cbc09346">SetupDiBuildDriverInfoList</a> to build a device's list of compatible drivers from its class driver list instead of the INF file.


##### - Flags.DI_DIDCLASS

Set if <a href="https://msdn.microsoft.com/9e377865-8029-41c1-85b9-fdb2cbc09346">SetupDiBuildDriverInfoList</a> has already built a list of the drivers for this class of device. If this list has already been built, it contains all the driver information and this flag is always set. <a href="https://msdn.microsoft.com/d8067609-1046-4641-9f57-b0ee2be5a3b2">SetupDiDestroyDriverInfoList</a> clears this flag when it deletes a list of drivers for a class.

This flag is read-only. Only the operating system sets this flag.


##### - Flags.DI_DIDCOMPAT

Set if <a href="https://msdn.microsoft.com/9e377865-8029-41c1-85b9-fdb2cbc09346">SetupDiBuildDriverInfoList</a> has already built a list of compatible drivers for this device. If this list has already been built, it contains all the driver information and this flag is always set. <a href="https://msdn.microsoft.com/d8067609-1046-4641-9f57-b0ee2be5a3b2">SetupDiDestroyDriverInfoList</a> clears this flag when it deletes a compatible driver list.

This flag is only set in device installation parameters that are associated with a particular device information element, not in parameters for a device information set as a whole.

This flag is read-only. Only the operating system sets this flag.


##### - Flags.DI_DONOTCALLCONFIGMG

Set if the configuration manager should not be called to remove or reenumerate devices during the execution of certain device installation functions (for example, <a href="https://msdn.microsoft.com/130a58a8-7964-40cb-87e8-4765178bd1ff">SetupDiInstallDevice</a>).

If this flag is set, device installation applications, class installers, and co-installers must not call the following functions:

<a href="https://msdn.microsoft.com/dcba5021-7517-4922-9c50-ebfa7375e258">CM_Reenumerate_DevNode</a>
<a href="https://msdn.microsoft.com/1d927aec-db3c-403f-9952-1bcc931984bf">CM_Reenumerate_DevNode_Ex</a>
<a href="https://msdn.microsoft.com/0a80cddd-d5be-42cb-ba11-0a3292b973a3">CM_Query_And_Remove_SubTree</a>
<a href="https://msdn.microsoft.com/c8a3af37-0886-4187-9cdb-49616bcb04a9">CM_Query_And_Remove_SubTree_Ex</a>
<a href="https://msdn.microsoft.com/94d0023d-d93f-42da-b2fc-54b9d8831b9b">CM_Setup_DevNode</a>
<a href="https://msdn.microsoft.com/831fdc18-1d5e-4358-8f64-59abb5e7c0e6">CM_Setup_DevNode_Ex</a>
<a href="https://msdn.microsoft.com/52c3b9b8-6d0d-4b4d-9be4-5bd0d864d2fd">CM_Set_HW_Prof_Flags</a>
<a href="https://msdn.microsoft.com/8e29d4d8-38a4-4656-b164-e214b0fc8b7d">CM_Set_HW_Prof_Flags_Ex</a>
<a href="https://msdn.microsoft.com/ddc3a507-03ee-4f44-89e3-64ec4290d0ff">CM_Enable_DevNode</a>
<a href="https://msdn.microsoft.com/582e7cdf-2302-4c9a-8834-5eada8f142d8">CM_Enable_DevNode_Ex</a>
<a href="https://msdn.microsoft.com/6013fec3-1fb3-4956-982d-5841518f5d31">CM_Disable_DevNode</a>
<a href="https://msdn.microsoft.com/d493399a-b9f7-44cc-9c0e-150137d468c8">CM_Disable_DevNode_Ex</a>

##### - Flags.DI_DRIVERPAGE_ADDED

Set by a class installer or co-installer if the installer supplies a page that replaces the system-supplied driver properties page. If this flag is set, the operating system does not display the system-supplied driver page.


##### - Flags.DI_ENUMSINGLEINF

Set if installers and other <a href="devinst.device_installation_components">device installation components</a> should only search the INF file specified by SP_DEVINSTALL_PARAMS.<b>DriverPath</b>. If this flag is set, <b>DriverPath</b> contains the path of a single INF file instead of a path of a directory.


##### - Flags.DI_INF_IS_SORTED

Set to indicate that the Select Device page should list drivers in the order in which they appear in the INF file, instead of sorting them alphabetically. 


##### - Flags.DI_INSTALLDISABLED

Set if the device should be installed in a disabled state by default. To be recognized, this flag must be set before Windows calls the default handler for the <a href="https://msdn.microsoft.com/2d369086-c2b6-45a4-a87e-51ff5725938f">DIF_INSTALLDEVICE</a> request. 


##### - Flags.DI_MULTMFGS

Set by <a href="https://msdn.microsoft.com/9e377865-8029-41c1-85b9-fdb2cbc09346">SetupDiBuildDriverInfoList</a> if a list of drivers for a <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff552344">device setup class</a> contains drivers that are provided by multiple manufacturers.

This flag is read-only. Only the operating system sets this flag.


##### - Flags.DI_NEEDREBOOT

For NT-based operating systems, this flag is set if the device requires that the computer be restarted after device installation or a device state change. A class installer or co-installer can set this flag at any time during device installation, if the installer determines that a restart is necessary.


##### - Flags.DI_NEEDRESTART

The same as DI_NEEDREBOOT.


##### - Flags.DI_NOBROWSE

Set to disable browsing when the user is selecting an OEM disk path. A device installation application sets this flag to constrain a user to only installing from the installation media location.


##### - Flags.DI_NODI_DEFAULTACTION

Set if <a href="https://msdn.microsoft.com/2aa631c3-8d00-4309-a37c-efaa7eda3efa">SetupDiCallClassInstaller</a> should not perform any default action if the class installer returns ERR_DI_DO_DEFAULT or there is not a class installer.


##### - Flags.DI_NOFILECOPY

Set if device installation applications and components, such as <a href="https://msdn.microsoft.com/130a58a8-7964-40cb-87e8-4765178bd1ff">SetupDiInstallDevice</a>, should skip file copying.


##### - Flags.DI_NOVCP

Set to disable creation of a new copy queue. Use the caller-supplied copy queue in SP_DEVINSTALL_PARAMS.<b>FileQueue</b>.


##### - Flags.DI_NOWRITE_IDS

Set to prevent <a href="https://msdn.microsoft.com/130a58a8-7964-40cb-87e8-4765178bd1ff">SetupDiInstallDevice</a> from writing the INF-specified <a href="devinst.hardware_ids">hardware IDs</a> and <a href="devinst.compatible_ids">compatible IDs</a> to the device properties for the device node (<a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">devnode</a>). This flag should only be set for root-enumerated devices. 

This flag overrides the DI_FLAGSEX_ALWAYSWRITEIDS flag.


##### - Flags.DI_PROPERTIES_CHANGE

Set by Device Manager if a device's properties were changed, which requires an update of the installer's user interface. 


##### - Flags.DI_QUIETINSTALL

Set if the device installer functions must be silent and use default choices wherever possible. Class installers and co-installers must not display any UI if this flag is set.


##### - Flags.DI_RESOURCEPAGE_ADDED

Set by a class installer or co-installer if the installer supplies a page that replaces the system-supplied resource properties page. If this flag is set, the operating system does not display the system-supplied resource page.


##### - Flags.DI_SHOWOEM

Set to allow support for OEM disks. If this flag is set, the operating system presents a "Have Disk" button on the Select Device page. This flag is set, by default, in system-supplied wizards.


##### - Flags.DI_USECI_SELECTSTRINGS

Set if a class installer or co-installer supplied strings that should be used during <a href="https://msdn.microsoft.com/c6a512ad-bcc6-4dc5-873e-33bdaab129e2">SetupDiSelectDevice</a>.


##### - FlagsEx.DI_FLAGSEX_ALLOWEXCLUDEDDRVS

If set, include drivers that were marked "Exclude From Select." 

For example, if this flag is set, <a href="https://msdn.microsoft.com/c6a512ad-bcc6-4dc5-873e-33bdaab129e2">SetupDiSelectDevice</a> displays drivers that have the Exclude From Select state and <a href="https://msdn.microsoft.com/9e377865-8029-41c1-85b9-fdb2cbc09346">SetupDiBuildDriverInfoList</a> includes Exclude From Select drivers in the requested driver list. 

A driver is "Exclude From Select" if either it is marked <b>ExcludeFromSelect</b> in the INF file or it is a driver for a device whose whole setup class is marked <b>NoInstallClass</b> or <b>NoUseClass</b> in the class installer INF. Drivers for PnP devices are typically "Exclude From Select"; PnP devices should not be manually installed. To build a list of driver files for a PnP device a caller of <b>SetupDiBuildDriverInfoList</b> must set this flag. 


##### - FlagsEx.DI_FLAGSEX_ALWAYSWRITEIDS

If set and the DI_NOWRITE_IDS flag is clear, always write hardware and compatible IDs to the device properties for the devnode. This flag should only be set for root-enumerated devices.


##### - FlagsEx.DI_FLAGSEX_APPENDDRIVERLIST

If set, <b>SetupDiBuildDriverInfoList</b> appends a new driver list to an existing list. This flag is relevant when searching multiple locations.


##### - FlagsEx.DI_FLAGSEX_CI_FAILED

Set by the operating system if a class installer failed to load or start. This flag is read-only.


##### - FlagsEx.DI_FLAGSEX_DIDCOMPATINFO

Windows has built a list of <a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">driver nodes</a> that are compatible with the device. This flag is read-only.


##### - FlagsEx.DI_FLAGSEX_DIDINFOLIST

Windows has built a list of driver nodes that includes all the drivers that are listed in the INF files of the specified setup class. If the specified setup class is <b>NULL</b> because the HDEVINFO set or device has no associated class, the list includes all driver nodes from all available INF files. This flag is read-only.


##### - FlagsEx.DI_FLAGSEX_DRIVERLIST_FROM_URL

If set, build the driver list from INF(s) retrieved from the URL that is specified in SP_DEVINSTALL_PARAMS.<b>DriverPath</b>. If the <b>DriverPath</b> is an empty string, use the Windows Update website.

Currently, the operating system does not support URLs. Use this flag to direct <b>SetupDiBuildDriverInfoList</b> to search the Windows Update website.

Do not set this flag if DI_QUIETINSTALL is set.


##### - FlagsEx.DI_FLAGSEX_EXCLUDE_OLD_INET_DRIVERS

If set, do not include old Internet drivers when building a driver list. This flag should be set any time that you are building a list of potential drivers for a device. You can clear this flag if you are just getting a list of drivers currently installed for a device. 


##### - FlagsEx.DI_FLAGSEX_FILTERCLASSES

If set, <a href="https://msdn.microsoft.com/a01b1f8f-55af-4053-8c31-9329ef36f2ce">SetupDiBuildClassInfoList</a> will check for class inclusion filters. This means that a device will not be included in the class list if its class is marked as NoInstallClass.


##### - FlagsEx.DI_FLAGSEX_FILTERSIMILARDRIVERS

(Windows XP and later.) If set, <a href="https://msdn.microsoft.com/9e377865-8029-41c1-85b9-fdb2cbc09346">SetupDiBuildDriverInfoList</a> includes "similar" drivers when building a class driver list. A "similar" driver is one for which one of the hardware IDs or compatible IDs in the INF file partially (or completely) matches one of the hardware IDs or compatible IDs of the hardware.


##### - FlagsEx.DI_FLAGSEX_INET_DRIVER

If set, the driver was obtained from the Internet. Windows will not use the device's INF to install future devices because Windows cannot guarantee that it can retrieve the driver files again from the Internet.


##### - FlagsEx.DI_FLAGSEX_INSTALLEDDRIVER

(Windows XP and later.) If set, <a href="https://msdn.microsoft.com/9e377865-8029-41c1-85b9-fdb2cbc09346">SetupDiBuildDriverInfoList</a> includes only the currently installed driver when creating a list of class drivers or device-compatible drivers.


##### - FlagsEx.DI_FLAGSEX_IN_SYSTEM_SETUP

If set, installation is occurring during initial system setup. This flag is read-only.


##### - FlagsEx.DI_FLAGSEX_NO_DRVREG_MODIFY

Do not process the <b>AddReg</b> and <b>DelReg</b> entries for the device's hardware and software (driver) keys. That is, the <b>AddReg</b> and <b>DelReg</b> entries in the INF file <i>DDInstall</i> and <i>DDInstall</i><b>.HW</b> sections.


##### - FlagsEx.DI_FLAGSEX_POWERPAGE_ADDED

If set, an installer added their own page for the power properties dialog. The operating system will not display the system-supplied power properties page. This flag is only relevant if the device supports power management.


##### - FlagsEx.DI_FLAGSEX_PROPCHANGE_PENDING

If set, the user made changes to one or more device property sheets. The property-page provider typically sets this flag.

When the user closes the device property sheet, Device Manager checks the DI_FLAGSEX_PROPCHANGE_PENDING flag. If it is set, Device Manager clears this flag, sets the DI_PROPERTIES_CHANGE flag, and sends a DIF_PROPERTYCHANGE request to the installers to notify them that something has changed.


##### - FlagsEx.DI_FLAGSEX_SETFAILEDINSTALL

Set if the installation failed. If this flag is set, the <a href="https://msdn.microsoft.com/130a58a8-7964-40cb-87e8-4765178bd1ff">SetupDiInstallDevice</a> function just sets the FAILEDINSTALL flag in the device's <b>ConfigFlags</b> registry value. If DI_FLAGSEX_SETFAILEDINSTALL is set, co-installers must return NO_ERROR in response to DIF_INSTALLDEVICE, while class installers must return NO_ERROR or ERROR_DI_DO_DEFAULT.


##### - FlagsEx.DI_FLAGSEX_USECLASSFORCOMPAT

Filter INF files on the device's setup class when building a list of compatible drivers. If a device's setup class is known, setting this flag reduces the time that is required to build a list of compatible drivers when searching INF files that are not precompiled. This flag is ignored if DI_COMPAT_FROM_CLASS is set.


## -see-also




<a href="https://msdn.microsoft.com/a01b1f8f-55af-4053-8c31-9329ef36f2ce">SetupDiBuildClassInfoList</a>



<a href="https://msdn.microsoft.com/9e377865-8029-41c1-85b9-fdb2cbc09346">SetupDiBuildDriverInfoList</a>



<a href="https://msdn.microsoft.com/2aa631c3-8d00-4309-a37c-efaa7eda3efa">SetupDiCallClassInstaller</a>



<a href="https://msdn.microsoft.com/e5e8c203-cf71-4cb4-a7a8-5af3a2483eea">SetupDiGetDeviceInstallParams</a>



<a href="https://msdn.microsoft.com/130a58a8-7964-40cb-87e8-4765178bd1ff">SetupDiInstallDevice</a>



<a href="https://msdn.microsoft.com/c6a512ad-bcc6-4dc5-873e-33bdaab129e2">SetupDiSelectDevice</a>



<a href="https://msdn.microsoft.com/20384538-e124-41f7-94a6-c0fb9f5fe6a0">SetupDiSetDeviceInstallParams</a>
 

 

