---
UID: NF:setupapi.SetupDiGetDeviceRegistryPropertyW
title: SetupDiGetDeviceRegistryPropertyW function
author: windows-sdk-content
description: The SetupDiGetDeviceRegistryProperty function retrieves a specified Plug and Play device property.
old-location: devinst\setupdigetdeviceregistryproperty.htm
tech.root: devinst
ms.assetid: d42269dc-57b5-4303-94d9-02f6ee16a96f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetupDiGetDeviceRegistryProperty, SetupDiGetDeviceRegistryProperty function [Device and Driver Installation], SetupDiGetDeviceRegistryPropertyA, SetupDiGetDeviceRegistryPropertyW, devinst.setupdigetdeviceregistryproperty, di-rtns_a60fa017-1c15-45bf-a178-37516bc0aea1.xml, setupapi/SetupDiGetDeviceRegistryProperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: DesktopFor universal, call CM_Get_DevNode_Registry_Property
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Setupapi.lib
 - Setupapi.dll
api_name:
 - SetupDiGetDeviceRegistryProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupDiGetDeviceRegistryPropertyW function


## -description


The <b>SetupDiGetDeviceRegistryProperty</b> function retrieves a specified Plug and Play device property.


## -parameters




### -param DeviceInfoSet [in]

A handle to a <a href="devinst.device_information_sets">device information set</a> that contains a device information element that represents the device for which to retrieve a Plug and Play property.


### -param DeviceInfoData [in]

A pointer to an <a href="https://msdn.microsoft.com/9ad0ef4f-4a67-4f16-8bb1-2242dad0d041">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>.


### -param Property [in]

One of the following values that specifies the property to be retrieved:





#### SPDRP_ADDRESS

The function retrieves the device's address.



#### SPDRP_BUSNUMBER

The function retrieves the device's bus number.



#### SPDRP_BUSTYPEGUID

The function retrieves the GUID for the device's bus type.



#### SPDRP_CAPABILITIES

The function retrieves a bitwise OR of the following CM_DEVCAP_<i>Xxx </i>flags in a DWORD. The device capabilities that are represented by these flags correspond to the device capabilities that are represented by the members of the <a href="https://msdn.microsoft.com/1edae050-8e72-42e7-9dc9-8f449699969c">DEVICE_CAPABILITIES</a> structure. The CM_DEVCAP_Xxx constants are defined in <i>Cfgmgr32.h.</i>

<table>
<tr>
<th>CM_DEVCAP_Xxx flag</th>
<th>Corresponding DEVICE_CAPABILITIES structure member</th>
</tr>
<tr>
<td>
CM_DEVCAP_LOCKSUPPORTED

</td>
<td>
<b>LockSupported </b>

</td>
</tr>
<tr>
<td>
CM_DEVCAP_EJECTSUPPORTED

</td>
<td>
<b>EjectSupported </b>

</td>
</tr>
<tr>
<td>
CM_DEVCAP_REMOVABLE

</td>
<td>
<b>Removable </b>

</td>
</tr>
<tr>
<td>
CM_DEVCAP_DOCKDEVICE

</td>
<td>
<b>DockDevice </b>

</td>
</tr>
<tr>
<td>
CM_DEVCAP_UNIQUEID

</td>
<td>
<b>UniqueID </b>

</td>
</tr>
<tr>
<td>
CM_DEVCAP_SILENTINSTALL

</td>
<td>
<b>SilentInstall </b>

</td>
</tr>
<tr>
<td>
CM_DEVCAP_RAWDEVICEOK

</td>
<td>
<b>RawDeviceOK </b>

</td>
</tr>
<tr>
<td>
CM_DEVCAP_SURPRISEREMOVALOK

</td>
<td>
<b>SurpriseRemovalOK </b>

</td>
</tr>
<tr>
<td>
CM_DEVCAP_HARDWAREDISABLED

</td>
<td>
<b>HardwareDisabled </b>

</td>
</tr>
<tr>
<td>
CM_DEVCAP_NONDYNAMIC

</td>
<td>
<b>NonDynamic</b>

</td>
</tr>
</table>
 



#### SPDRP_CHARACTERISTICS

The function retrieves a bitwise OR of a device's characteristics flags in a DWORD. For a description of these flags, which are defined in <i>Wdm.h</i> and <i>Ntddk.h</i>, see the <i>DeviceCharacteristics</i> parameter of the <a href="https://msdn.microsoft.com/54ca9dc8-8095-4b62-9ebc-f297abb429ca">IoCreateDevice</a> function.



#### SPDRP_CLASS

The function retrieves a REG_SZ string that contains the <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff552344">device setup class</a> of a device.



#### SPDRP_CLASSGUID

The function retrieves a REG_SZ string that contains the GUID that represents the device setup class of a device.



#### SPDRP_COMPATIBLEIDS

The function retrieves a REG_MULTI_SZ string that contains the list of compatible IDs for a device. For information about compatible IDs, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/install/device-identification-strings">Device Identification Strings</a>.



#### SPDRP_CONFIGFLAGS

The function retrieves a bitwise OR of a device's configuration flags in a DWORD value. The configuration flags are represented by the CONFIGFLAG_<i>Xxx</i> bitmasks that are defined in <i>Regstr.h</i>.



#### SPDRP_DEVICE_POWER_DATA

(Windows XP and later) The function retrieves a <a href="https://msdn.microsoft.com/38fea22b-4d9a-4b03-bbb7-c22578f60def">CM_POWER_DATA</a> structure that contains the device's power management information.



#### SPDRP_DEVICEDESC

The function retrieves a REG_SZ string that contains the description of a device. 



#### SPDRP_DEVTYPE

The function retrieves a DWORD value that represents the device's type. For more information, see <a href="https://msdn.microsoft.com/32e179f9-ab11-4360-b2fd-4276c6b6b3a0">Specifying Device Types</a>.



#### SPDRP_DRIVER

The function retrieves a string that identifies the device's <a href="https://msdn.microsoft.com/5f6fec1a-1134-4765-81be-9b50939e5e66">software key</a> (sometimes called the <a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">driver key</a>). For more information about driver keys, see <a href="devinst.registry_trees_and_keys">Registry Trees and Keys for Devices and Drivers</a>.



#### SPDRP_ENUMERATOR_NAME

The function retrieves a REG_SZ string that contains the name of the device's <a href="https://msdn.microsoft.com/0dd010e7-3e10-422a-adcb-8fe7df9e29ab">enumerator</a>.



#### SPDRP_EXCLUSIVE

The function retrieves a DWORD value that indicates whether a user can obtain exclusive use of the device. The returned value is one if exclusive use is allowed, or zero otherwise. For more information, see <a href="https://msdn.microsoft.com/54ca9dc8-8095-4b62-9ebc-f297abb429ca">IoCreateDevice</a>.



#### SPDRP_FRIENDLYNAME

The function retrieves a REG_SZ string that contains the friendly name of a device.



#### SPDRP_HARDWAREID

The function retrieves a REG_MULTI_SZ string that contains the list of hardware IDs for a device. For information about hardware IDs, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/install/device-identification-strings">Device Identification Strings</a>.



#### SPDRP_INSTALL_STATE

(Windows XP and later) The function retrieves a DWORD value that indicates the installation state of a device. The installation state is represented by one of the CM_INSTALL_STATE_<i>Xxx</i> values that are defined in <i>Cfgmgr32.h</i>. The CM_INSTALL_STATE_<i>Xxx</i> values correspond to the <a href="https://msdn.microsoft.com/82b702ae-ea62-4bc1-ad92-467eba027e3d">DEVICE_INSTALL_STATE</a> enumeration values. 



#### SPDRP_LEGACYBUSTYPE

The function retrieves the device's legacy bus type as an INTERFACE_TYPE value (defined in <i>Wdm.h</i> and <i>Ntddk.h</i>).



#### SPDRP_LOCATION_INFORMATION

The function retrieves a REG_SZ string that contains the hardware location of a device. 



#### SPDRP_LOCATION_PATHS

(Windows Server 2003 and later) The function retrieves a REG_MULTI_SZ string that represents the location of the device in the device tree.



#### SPDRP_LOWERFILTERS

The function retrieves a REG_MULTI_SZ string that contains the names of a device's lower-filter drivers.



#### SPDRP_MFG

The function retrieves a REG_SZ string that contains the name of the device manufacturer.



#### SPDRP_PHYSICAL_DEVICE_OBJECT_NAME

The function retrieves a REG_SZ string that contains the name that is associated with the device's PDO. For more information, see <a href="https://msdn.microsoft.com/54ca9dc8-8095-4b62-9ebc-f297abb429ca">IoCreateDevice</a>.



#### SPDRP_REMOVAL_POLICY

(Windows XP and later) The function retrieves the device's current removal policy as a DWORD that contains one of the CM_REMOVAL_POLICY_<i>Xxx</i> values that are defined in <i>Cfgmgr32.h</i>.



#### SPDRP_REMOVAL_POLICY_HW_DEFAULT

(Windows XP and later) The function retrieves the device's hardware-specified default removal policy as a DWORD that contains one of the CM_REMOVAL_POLICY_<i>Xxx</i> values that are defined in <i>Cfgmgr32.h</i>.



#### SPDRP_REMOVAL_POLICY_OVERRIDE

(Windows XP and later) The function retrieves the device's override removal policy (if it exists) from the registry, as a DWORD that contains one of the CM_REMOVAL_POLICY_<i>Xxx</i> values that are defined in <i>Cfgmgr32.h</i>.



#### SPDRP_SECURITY

The function retrieves a <a href="https://msdn.microsoft.com/0af0685c-d3a3-4c76-8fca-fb38f60411bf">SECURITY_DESCRIPTOR</a> structure for a device.



#### SPDRP_SECURITY_SDS

The function retrieves a REG_SZ string that contains the device's security descriptor. For information about security descriptor strings, see <a href="https://msdn.microsoft.com/2b15325e-34ed-497b-ae6d-3ec3ac168232">Security Descriptor Definition Language (Windows)</a>. For information about the format of security descriptor strings, see Security Descriptor Definition Language (Windows).



#### SPDRP_SERVICE

The function retrieves a REG_SZ string that contains the service name for a device.



#### SPDRP_UI_NUMBER

The function retrieves a DWORD value set to the value of the <b>UINumber</b> member of the device's <a href="https://msdn.microsoft.com/1edae050-8e72-42e7-9dc9-8f449699969c">DEVICE_CAPABILITIES</a> structure.



#### SPDRP_UI_NUMBER_DESC_FORMAT

The function retrieves a format string (REG_SZ) used to display the <b>UINumber</b> value.



#### SPDRP_UPPERFILTERS

The function retrieves a REG_MULTI_SZ string that contains the names of a device's upper filter drivers.


### -param PropertyRegDataType [out, optional]

A pointer to a variable that receives the data type of the property that is being retrieved. This is one of the standard registry data types. This parameter is optional and can be <b>NULL</b>.


### -param PropertyBuffer [out, optional]

A pointer to a buffer that receives the property that is being retrieved. If this parameter is set to <b>NULL</b>, and <i>PropertyBufferSize</i> is also set to zero, the function returns the required size for the buffer in <i>RequiredSize</i>.


### -param PropertyBufferSize [in]

The size, in bytes, of the <i>PropertyBuffer </i>buffer.


### -param RequiredSize [out, optional]

A pointer to a variable of type DWORD that receives the required size, in bytes, of the <i>PropertyBuffer</i> buffer that is required to hold the data for the requested property. This parameter is optional and can be <b>NULL</b>.


##### - Property.SPDRP_ADDRESS

The function retrieves the device's address.


##### - Property.SPDRP_BUSNUMBER

The function retrieves the device's bus number.


##### - Property.SPDRP_BUSTYPEGUID

The function retrieves the GUID for the device's bus type.


##### - Property.SPDRP_CAPABILITIES

The function retrieves a bitwise OR of the following CM_DEVCAP_<i>Xxx </i>flags in a DWORD. The device capabilities that are represented by these flags correspond to the device capabilities that are represented by the members of the <a href="https://msdn.microsoft.com/1edae050-8e72-42e7-9dc9-8f449699969c">DEVICE_CAPABILITIES</a> structure. The CM_DEVCAP_Xxx constants are defined in <i>Cfgmgr32.h.</i>

<table>
<tr>
<th>CM_DEVCAP_Xxx flag</th>
<th>Corresponding DEVICE_CAPABILITIES structure member</th>
</tr>
<tr>
<td>
CM_DEVCAP_LOCKSUPPORTED

</td>
<td>
<b>LockSupported </b>

</td>
</tr>
<tr>
<td>
CM_DEVCAP_EJECTSUPPORTED

</td>
<td>
<b>EjectSupported </b>

</td>
</tr>
<tr>
<td>
CM_DEVCAP_REMOVABLE

</td>
<td>
<b>Removable </b>

</td>
</tr>
<tr>
<td>
CM_DEVCAP_DOCKDEVICE

</td>
<td>
<b>DockDevice </b>

</td>
</tr>
<tr>
<td>
CM_DEVCAP_UNIQUEID

</td>
<td>
<b>UniqueID </b>

</td>
</tr>
<tr>
<td>
CM_DEVCAP_SILENTINSTALL

</td>
<td>
<b>SilentInstall </b>

</td>
</tr>
<tr>
<td>
CM_DEVCAP_RAWDEVICEOK

</td>
<td>
<b>RawDeviceOK </b>

</td>
</tr>
<tr>
<td>
CM_DEVCAP_SURPRISEREMOVALOK

</td>
<td>
<b>SurpriseRemovalOK </b>

</td>
</tr>
<tr>
<td>
CM_DEVCAP_HARDWAREDISABLED

</td>
<td>
<b>HardwareDisabled </b>

</td>
</tr>
<tr>
<td>
CM_DEVCAP_NONDYNAMIC

</td>
<td>
<b>NonDynamic</b>

</td>
</tr>
</table>
 


##### - Property.SPDRP_CHARACTERISTICS

The function retrieves a bitwise OR of a device's characteristics flags in a DWORD. For a description of these flags, which are defined in <i>Wdm.h</i> and <i>Ntddk.h</i>, see the <i>DeviceCharacteristics</i> parameter of the <a href="https://msdn.microsoft.com/54ca9dc8-8095-4b62-9ebc-f297abb429ca">IoCreateDevice</a> function.


##### - Property.SPDRP_CLASS

The function retrieves a REG_SZ string that contains the <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff552344">device setup class</a> of a device.


##### - Property.SPDRP_CLASSGUID

The function retrieves a REG_SZ string that contains the GUID that represents the device setup class of a device.


##### - Property.SPDRP_COMPATIBLEIDS

The function retrieves a REG_MULTI_SZ string that contains the list of compatible IDs for a device. For information about compatible IDs, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/install/device-identification-strings">Device Identification Strings</a>.


##### - Property.SPDRP_CONFIGFLAGS

The function retrieves a bitwise OR of a device's configuration flags in a DWORD value. The configuration flags are represented by the CONFIGFLAG_<i>Xxx</i> bitmasks that are defined in <i>Regstr.h</i>.


##### - Property.SPDRP_DEVICEDESC

The function retrieves a REG_SZ string that contains the description of a device. 


##### - Property.SPDRP_DEVICE_POWER_DATA

(Windows XP and later) The function retrieves a <a href="https://msdn.microsoft.com/38fea22b-4d9a-4b03-bbb7-c22578f60def">CM_POWER_DATA</a> structure that contains the device's power management information.


##### - Property.SPDRP_DEVTYPE

The function retrieves a DWORD value that represents the device's type. For more information, see <a href="https://msdn.microsoft.com/32e179f9-ab11-4360-b2fd-4276c6b6b3a0">Specifying Device Types</a>.


##### - Property.SPDRP_DRIVER

The function retrieves a string that identifies the device's <a href="https://msdn.microsoft.com/5f6fec1a-1134-4765-81be-9b50939e5e66">software key</a> (sometimes called the <a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">driver key</a>). For more information about driver keys, see <a href="devinst.registry_trees_and_keys">Registry Trees and Keys for Devices and Drivers</a>.


##### - Property.SPDRP_ENUMERATOR_NAME

The function retrieves a REG_SZ string that contains the name of the device's <a href="https://msdn.microsoft.com/0dd010e7-3e10-422a-adcb-8fe7df9e29ab">enumerator</a>.


##### - Property.SPDRP_EXCLUSIVE

The function retrieves a DWORD value that indicates whether a user can obtain exclusive use of the device. The returned value is one if exclusive use is allowed, or zero otherwise. For more information, see <a href="https://msdn.microsoft.com/54ca9dc8-8095-4b62-9ebc-f297abb429ca">IoCreateDevice</a>.


##### - Property.SPDRP_FRIENDLYNAME

The function retrieves a REG_SZ string that contains the friendly name of a device.


##### - Property.SPDRP_HARDWAREID

The function retrieves a REG_MULTI_SZ string that contains the list of hardware IDs for a device. For information about hardware IDs, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/install/device-identification-strings">Device Identification Strings</a>.


##### - Property.SPDRP_INSTALL_STATE

(Windows XP and later) The function retrieves a DWORD value that indicates the installation state of a device. The installation state is represented by one of the CM_INSTALL_STATE_<i>Xxx</i> values that are defined in <i>Cfgmgr32.h</i>. The CM_INSTALL_STATE_<i>Xxx</i> values correspond to the <a href="https://msdn.microsoft.com/82b702ae-ea62-4bc1-ad92-467eba027e3d">DEVICE_INSTALL_STATE</a> enumeration values. 


##### - Property.SPDRP_LEGACYBUSTYPE

The function retrieves the device's legacy bus type as an INTERFACE_TYPE value (defined in <i>Wdm.h</i> and <i>Ntddk.h</i>).


##### - Property.SPDRP_LOCATION_INFORMATION

The function retrieves a REG_SZ string that contains the hardware location of a device. 


##### - Property.SPDRP_LOCATION_PATHS

(Windows Server 2003 and later) The function retrieves a REG_MULTI_SZ string that represents the location of the device in the device tree.


##### - Property.SPDRP_LOWERFILTERS

The function retrieves a REG_MULTI_SZ string that contains the names of a device's lower-filter drivers.


##### - Property.SPDRP_MFG

The function retrieves a REG_SZ string that contains the name of the device manufacturer.


##### - Property.SPDRP_PHYSICAL_DEVICE_OBJECT_NAME

The function retrieves a REG_SZ string that contains the name that is associated with the device's PDO. For more information, see <a href="https://msdn.microsoft.com/54ca9dc8-8095-4b62-9ebc-f297abb429ca">IoCreateDevice</a>.


##### - Property.SPDRP_REMOVAL_POLICY

(Windows XP and later) The function retrieves the device's current removal policy as a DWORD that contains one of the CM_REMOVAL_POLICY_<i>Xxx</i> values that are defined in <i>Cfgmgr32.h</i>.


##### - Property.SPDRP_REMOVAL_POLICY_HW_DEFAULT

(Windows XP and later) The function retrieves the device's hardware-specified default removal policy as a DWORD that contains one of the CM_REMOVAL_POLICY_<i>Xxx</i> values that are defined in <i>Cfgmgr32.h</i>.


##### - Property.SPDRP_REMOVAL_POLICY_OVERRIDE

(Windows XP and later) The function retrieves the device's override removal policy (if it exists) from the registry, as a DWORD that contains one of the CM_REMOVAL_POLICY_<i>Xxx</i> values that are defined in <i>Cfgmgr32.h</i>.


##### - Property.SPDRP_SECURITY

The function retrieves a <a href="https://msdn.microsoft.com/0af0685c-d3a3-4c76-8fca-fb38f60411bf">SECURITY_DESCRIPTOR</a> structure for a device.


##### - Property.SPDRP_SECURITY_SDS

The function retrieves a REG_SZ string that contains the device's security descriptor. For information about security descriptor strings, see <a href="https://msdn.microsoft.com/2b15325e-34ed-497b-ae6d-3ec3ac168232">Security Descriptor Definition Language (Windows)</a>. For information about the format of security descriptor strings, see Security Descriptor Definition Language (Windows).


##### - Property.SPDRP_SERVICE

The function retrieves a REG_SZ string that contains the service name for a device.


##### - Property.SPDRP_UI_NUMBER

The function retrieves a DWORD value set to the value of the <b>UINumber</b> member of the device's <a href="https://msdn.microsoft.com/1edae050-8e72-42e7-9dc9-8f449699969c">DEVICE_CAPABILITIES</a> structure.


##### - Property.SPDRP_UI_NUMBER_DESC_FORMAT

The function retrieves a format string (REG_SZ) used to display the <b>UINumber</b> value.


##### - Property.SPDRP_UPPERFILTERS

The function retrieves a REG_MULTI_SZ string that contains the names of a device's upper filter drivers.


## -returns



<b>SetupDiGetDeviceRegistryProperty</b> returns <b>TRUE</b> if the call was successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by making a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>. <b>SetupDiGetDeviceRegistryProperty</b> returns the ERROR_INVALID_DATA error code if the requested property does not exist for a device or if the property data is not valid.




## -see-also




<a href="https://msdn.microsoft.com/8c3b7f81-ea6e-47ae-a396-58826d097f1f">IoGetDeviceProperty</a>



<a href="https://msdn.microsoft.com/79a600af-15c1-4afc-a2cd-568b97d979dc">SetupDiGetClassRegistryProperty</a>



<a href="https://msdn.microsoft.com/78457461-11ef-44ec-aa60-1adf4a48db8c">SetupDiSetClassRegistryProperty</a>



<a href="https://msdn.microsoft.com/2686f416-3eb5-4e6b-87c8-ab10608ab406">SetupDiSetDeviceRegistryProperty</a>
 

 

