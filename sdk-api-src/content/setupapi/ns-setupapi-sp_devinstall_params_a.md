---
UID: NS:setupapi._SP_DEVINSTALL_PARAMS_A
title: SP_DEVINSTALL_PARAMS_A (setupapi.h)
description: An SP_DEVINSTALL_PARAMS structure contains device installation parameters associated with a particular device information element or associated globally with a device information set. (ANSI)
helpviewer_keywords: ["*PSP_DEVINSTALL_PARAMS_A","PSP_DEVINSTALL_PARAMS","PSP_DEVINSTALL_PARAMS structure pointer [Device and Driver Installation]","SP_DEVINSTALL_PARAMS","SP_DEVINSTALL_PARAMS structure [Device and Driver Installation]","SP_DEVINSTALL_PARAMS_A","devinst.sp_devinstall_params","di-struct_ef7906d1-6416-41fc-8844-53f2f594a913.xml","setupapi/PSP_DEVINSTALL_PARAMS","setupapi/SP_DEVINSTALL_PARAMS"]
old-location: devinst\sp_devinstall_params.htm
tech.root: devinst
ms.assetid: 1bd21150-f8f4-480d-a4b2-99fa4b4233b9
ms.date: 10/26/2021
ms.keywords: '*PSP_DEVINSTALL_PARAMS_A, PSP_DEVINSTALL_PARAMS, PSP_DEVINSTALL_PARAMS structure pointer [Device and Driver Installation], SP_DEVINSTALL_PARAMS, SP_DEVINSTALL_PARAMS structure [Device and Driver Installation], SP_DEVINSTALL_PARAMS_A, devinst.sp_devinstall_params, di-struct_ef7906d1-6416-41fc-8844-53f2f594a913.xml, setupapi/PSP_DEVINSTALL_PARAMS, setupapi/SP_DEVINSTALL_PARAMS'
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
req.typenames: SP_DEVINSTALL_PARAMS_A, *PSP_DEVINSTALL_PARAMS_A
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SP_DEVINSTALL_PARAMS_A
 - setupapi/_SP_DEVINSTALL_PARAMS_A
 - PSP_DEVINSTALL_PARAMS_A
 - setupapi/PSP_DEVINSTALL_PARAMS_A
 - SP_DEVINSTALL_PARAMS_A
 - setupapi/SP_DEVINSTALL_PARAMS_A
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - setupapi.h
api_name:
 - SP_DEVINSTALL_PARAMS - sp_devinstall_params_a
---

# SP_DEVINSTALL_PARAMS_A structure


## -description

An SP_DEVINSTALL_PARAMS structure contains device installation parameters associated with a particular device information element or associated globally with a device information set.

## -struct-fields

### -field cbSize

The size, in bytes, of the SP_DEVINSTALL_PARAMS structure.

### -field Flags

Flags that control installation and user interface operations. Some flags can be set before sending the device installation request while other flags are set automatically during the processing of some requests. <b>Flags</b> can be a combination of the following values. 

The flag values are listed in groups: writable by <a href="/windows-hardware/drivers/">device installation applications</a> and installers, read-only (only set by the OS), reserved, and obsolete. The first group lists flags that are writable:





#### DI_CLASSINSTALLPARAMS

Set to use the Class Install parameters. <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdisetclassinstallparamsa">SetupDiSetClassInstallParams</a> sets this flag when the caller specifies parameters and clears the flag when the caller specifies a <b>NULL</b> parameters pointer. 



#### DI_COMPAT_FROM_CLASS

Set to force <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdibuilddriverinfolist">SetupDiBuildDriverInfoList</a> to build a device's list of compatible drivers from its class driver list instead of the INF file.



#### DI_DRIVERPAGE_ADDED

Set by a class installer or co-installer if the installer supplies a page that replaces the system-supplied driver properties page. If this flag is set, the operating system does not display the system-supplied driver page.



#### DI_DONOTCALLCONFIGMG

Set if the configuration manager should not be called to remove or reenumerate devices during the execution of certain device installation functions (for example, <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiinstalldevice">SetupDiInstallDevice</a>).

If this flag is set, device installation applications, class installers, and co-installers must not call the following functions:

<a href="../cfgmgr32/nf-cfgmgr32-cm_reenumerate_devnode.md">CM_Reenumerate_DevNode</a>
<a href="../cfgmgr32/nf-cfgmgr32-cm_reenumerate_devnode_ex.md">CM_Reenumerate_DevNode_Ex</a>
<a href="../cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtreew.md">CM_Query_And_Remove_SubTree</a>
<a href="../cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtree_exw.md">CM_Query_And_Remove_SubTree_Ex</a>
<a href="../cfgmgr32/nf-cfgmgr32-cm_setup_devnode.md">CM_Setup_DevNode</a>
<a href="../cfgmgr32/nf-cfgmgr32-cm_setup_devnode_ex.md">CM_Setup_DevNode_Ex</a>
<a href="../cfgmgr32/nf-cfgmgr32-cm_get_hw_prof_flagsw.md">CM_Set_HW_Prof_Flags</a>
<a href="../cfgmgr32/nf-cfgmgr32-cm_get_hw_prof_flags_exw.md">CM_Set_HW_Prof_Flags_Ex</a>
<a href="../cfgmgr32/nf-cfgmgr32-cm_enable_devnode.md">CM_Enable_DevNode</a>
<a href="../cfgmgr32/nf-cfgmgr32-cm_enable_devnode_ex.md">CM_Enable_DevNode_Ex</a>
<a href="../cfgmgr32/nf-cfgmgr32-cm_disable_devnode.md">CM_Disable_DevNode</a>
<a href="../cfgmgr32/nf-cfgmgr32-cm_disable_devnode_ex.md">CM_Disable_DevNode_Ex</a>


#### DI_ENUMSINGLEINF

Set if installers and other <a href="/windows-hardware/drivers/install/system-provided-device-installation-components">device installation components</a> should only search the INF file specified by SP_DEVINSTALL_PARAMS.<b>DriverPath</b>. If this flag is set, <b>DriverPath</b> contains the path of a single INF file instead of a path of a directory.



#### DI_INF_IS_SORTED

Set to indicate that the Select Device page should list drivers in the order in which they appear in the INF file, instead of sorting them alphabetically. 



#### DI_INSTALLDISABLED

Set if the device should be installed in a disabled state by default. To be recognized, this flag must be set before Windows calls the default handler for the <a href="/windows-hardware/drivers/install/dif-installdevice">DIF_INSTALLDEVICE</a> request. 



#### DI_NEEDREBOOT

For NT-based operating systems, this flag is set if the device requires that the computer be restarted after device installation or a device state change. A class installer or co-installer can set this flag at any time during device installation, if the installer determines that a restart is necessary.



#### DI_NEEDRESTART

The same as DI_NEEDREBOOT.



#### DI_NOBROWSE

Set to disable browsing when the user is selecting an OEM disk path. A device installation application sets this flag to constrain a user to only installing from the installation media location.



#### DI_NODI_DEFAULTACTION

Set if <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicallclassinstaller">SetupDiCallClassInstaller</a> should not perform any default action if the class installer returns ERR_DI_DO_DEFAULT or there is not a class installer.



#### DI_NOFILECOPY

Set if device installation applications and components, such as <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiinstalldevice">SetupDiInstallDevice</a>, should skip file copying.



#### DI_NOVCP

Set to disable creation of a new copy queue. Use the caller-supplied copy queue in SP_DEVINSTALL_PARAMS.<b>FileQueue</b>.



#### DI_NOWRITE_IDS

Set to prevent <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiinstalldevice">SetupDiInstallDevice</a> from writing the INF-specified <a href="/windows-hardware/drivers/install/hardware-ids">hardware IDs</a> and <a href="/windows-hardware/drivers/install/compatible-ids">compatible IDs</a> to the device properties for the device node (<a href="/windows-hardware/drivers/">devnode</a>). This flag should only be set for root-enumerated devices. 

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

Set if a class installer or co-installer supplied strings that should be used during <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiselectdevice">SetupDiSelectDevice</a>.

The following flags are read-only (only set by the OS):





#### DI_DIDCLASS

Set if <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdibuilddriverinfolist">SetupDiBuildDriverInfoList</a> has already built a list of the drivers for this class of device. If this list has already been built, it contains all the driver information and this flag is always set. <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdidestroydriverinfolist">SetupDiDestroyDriverInfoList</a> clears this flag when it deletes a list of drivers for a class.

This flag is read-only. Only the operating system sets this flag.



#### DI_DIDCOMPAT

Set if <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdibuilddriverinfolist">SetupDiBuildDriverInfoList</a> has already built a list of compatible drivers for this device. If this list has already been built, it contains all the driver information and this flag is always set. <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdidestroydriverinfolist">SetupDiDestroyDriverInfoList</a> clears this flag when it deletes a compatible driver list.

This flag is only set in device installation parameters that are associated with a particular device information element, not in parameters for a device information set as a whole.

This flag is read-only. Only the operating system sets this flag.



#### DI_MULTMFGS

Set by <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdibuilddriverinfolist">SetupDiBuildDriverInfoList</a> if a list of drivers for a <a href="/windows-hardware/drivers/install/overview-of-device-setup-classes">device setup class</a> contains drivers that are provided by multiple manufacturers.

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

For example, if this flag is set, <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiselectdevice">SetupDiSelectDevice</a> displays drivers that have the Exclude From Select state and <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdibuilddriverinfolist">SetupDiBuildDriverInfoList</a> includes Exclude From Select drivers in the requested driver list. 

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

If set, <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdibuildclassinfolist">SetupDiBuildClassInfoList</a> will check for class inclusion filters. This means that a device will not be included in the class list if its class is marked as NoInstallClass.



#### DI_FLAGSEX_FILTERSIMILARDRIVERS

(Windows XP and later.) If set, <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdibuilddriverinfolist">SetupDiBuildDriverInfoList</a> includes "similar" drivers when building a class driver list. A "similar" driver is one for which one of the hardware IDs or compatible IDs in the INF file partially (or completely) matches one of the hardware IDs or compatible IDs of the hardware.



#### DI_FLAGSEX_FINISHINSTALL_ACTION

(Windows Vista and later.) See <a href="/windows-hardware/drivers/install/setting-the-configflag-finishinstall-action-device-configuration-flag">Marking a Device as having a Finish-Install Action to Perform</a> for more information.



#### DI_FLAGSEX_INET_DRIVER

If set, the driver was obtained from the Internet. Windows will not use the device's INF to install future devices because Windows cannot guarantee that it can retrieve the driver files again from the Internet.



#### DI_FLAGSEX_INSTALLEDDRIVER

(Windows XP and later.) If set, <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdibuilddriverinfolist">SetupDiBuildDriverInfoList</a> includes only the currently installed driver when creating a list of class drivers or device-compatible drivers.



#### DI_FLAGSEX_NO_CLASSLIST_NODE_MERGE

(Windows XP and later.) If set, when creating a list of class drivers, <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdibuilddriverinfolist">SetupDiBuildDriverInfoList</a> will not merge nodes in the driver list that are from the same INF and have the same driver description and rank.



#### DI_FLAGSEX_NO_DRVREG_MODIFY

Do not process the <b>AddReg</b> and <b>DelReg</b> entries for the device's hardware and software (driver) keys. That is, the <b>AddReg</b> and <b>DelReg</b> entries in the INF file <i>DDInstall</i> and <i>DDInstall</i><b>.HW</b> sections.



#### DI_FLAGSEX_POWERPAGE_ADDED

If set, an installer added their own page for the power properties dialog. The operating system will not display the system-supplied power properties page. This flag is only relevant if the device supports power management.



#### DI_FLAGSEX_PROPCHANGE_PENDING

If set, the user made changes to one or more device property sheets. The property-page provider typically sets this flag.

When the user closes the device property sheet, Device Manager checks the DI_FLAGSEX_PROPCHANGE_PENDING flag. If it is set, Device Manager clears this flag, sets the DI_PROPERTIES_CHANGE flag, and sends a DIF_PROPERTYCHANGE request to the installers to notify them that something has changed.



#### DI_FLAGSEX_RECURSIVESEARCH

(Windows Vista and later.) If set, when <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdibuilddriverinfolist">SetupDiBuildDriverInfoList</a> searches for INFs in the path specified in the <i>DriverPath</i> value, the search will be recursive.



#### DI_FLAGSEX_SEARCH_PUBLISHED_INFS

(Windows Vista and later.) If set, when <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdibuilddriverinfolist">SetupDiBuildDriverInfoList</a> is used to search for INFs without an INF path or search path specified, this restricts the search to only INFs that have been imported into the Driver Store.



#### DI_FLAGSEX_SETFAILEDINSTALL

Set if the installation failed. If this flag is set, the <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiinstalldevice">SetupDiInstallDevice</a> function just sets the FAILEDINSTALL flag in the device's <b>ConfigFlags</b> registry value. If DI_FLAGSEX_SETFAILEDINSTALL is set, co-installers must return NO_ERROR in response to DIF_INSTALLDEVICE, while class installers must return NO_ERROR or ERROR_DI_DO_DEFAULT.



#### DI_FLAGSEX_USECLASSFORCOMPAT

Filter INF files on the device's setup class when building a list of compatible drivers. If a device's setup class is known, setting this flag reduces the time that is required to build a list of compatible drivers when searching INF files that are not precompiled. This flag is ignored if DI_COMPAT_FROM_CLASS is set.

The following flags are read-only; only the operating system sets these flags:





#### DI_FLAGSEX_CI_FAILED

Set by the operating system if a class installer failed to load or start. This flag is read-only.



#### DI_FLAGSEX_DIDCOMPATINFO

Windows has built a list of <a href="/windows-hardware/drivers/">driver nodes</a> that are compatible with the device. This flag is read-only.



#### DI_FLAGSEX_DIDINFOLIST

Windows has built a list of driver nodes that includes all the drivers that are listed in the INF files of the specified setup class. If the specified setup class is <b>NULL</b> because the HDEVINFO set or device has no associated class, the list includes all driver nodes from all available INF files. This flag is read-only.



#### DI_FLAGSEX_IN_SYSTEM_SETUP

If set, installation is occurring during initial system setup. This flag is read-only.

The following flags are reserved and should not be used:

DI_FLAGSEX_ALTPLATFORM_DRVSEARCH

DI_FLAGSEX_BACKUPONREPLACE 

DI_FLAGSEX_DEVICECHANGE 

DI_FLAGSEX_OLDINF_IN_CLASSLIST 

DI_FLAGSEX_PREINSTALLBACKUP 

DI_FLAGSEX_RESTART_DEVICE_ONLY

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

If you associate a file queue with a device information set (<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdisetdeviceinstallparamsa">SetupDiSetDeviceInstallParams</a>), you must disassociate the queue from the device information set before you delete the device information set. If you fail to disassociate the file queue, Windows cannot decrement its reference count on the device information set and cannot free the memory.

This queue is only used if the DI_NOVCP flag is set, indicating that file operations should be enqueued but not committed.

### -field ClassInstallReserved

A pointer for class-installer data. Co-installers must not use this field.

### -field Reserved

Reserved. For internal use only.

### -field DriverPath

This path is used by the <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdibuilddriverinfolist">SetupDiBuildDriverInfoList</a> function.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdibuildclassinfolist">SetupDiBuildClassInfoList</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdibuilddriverinfolist">SetupDiBuildDriverInfoList</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicallclassinstaller">SetupDiCallClassInstaller</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdeviceinstallparamsa">SetupDiGetDeviceInstallParams</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiinstalldevice">SetupDiInstallDevice</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiselectdevice">SetupDiSelectDevice</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdisetdeviceinstallparamsa">SetupDiSetDeviceInstallParams</a>

## -remarks

> [!NOTE]
> The setupapi.h header defines SP_DEVINSTALL_PARAMS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
