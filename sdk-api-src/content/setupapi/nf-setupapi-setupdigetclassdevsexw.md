---
UID: NF:setupapi.SetupDiGetClassDevsExW
title: SetupDiGetClassDevsExW function (setupapi.h)
description: The SetupDiGetClassDevsEx function returns a handle to a device information set that contains requested device information elements for a local or a remote computer. (Unicode)
helpviewer_keywords: ["SetupDiGetClassDevsEx", "SetupDiGetClassDevsEx function [Device and Driver Installation]", "SetupDiGetClassDevsExW", "devinst.setupdigetclassdevsex", "di-rtns_61e59e92-0451-4398-88af-0a14347aa74e.xml", "setupapi/SetupDiGetClassDevsEx"]
old-location: devinst\setupdigetclassdevsex.htm
tech.root: devinst
ms.assetid: 9f13ffe1-1a60-4d9a-942d-63312ca9bc5b
ms.date: 01/30/2023
ms.keywords: SetupDiGetClassDevsEx, SetupDiGetClassDevsEx function [Device and Driver Installation], SetupDiGetClassDevsExA, SetupDiGetClassDevsExW, devinst.setupdigetclassdevsex, di-rtns_61e59e92-0451-4398-88af-0a14347aa74e.xml, setupapi/SetupDiGetClassDevsEx
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupDiGetClassDevsExW
 - setupapi/SetupDiGetClassDevsExW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - ext-ms-win-setupapi-devobj-l1-1-0.dll
 - Setupapi.lib
 - Setupapi.dll
api_name:
 - SetupDiGetClassDevsEx
 - SetupDiGetClassDevsExW
---

# SetupDiGetClassDevsExW function


## -description

The <b>SetupDiGetClassDevsEx</b> function returns a handle to a <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains requested device information elements for a local or a remote computer.

## -parameters

### -param ClassGuid [in, optional]

A pointer to the GUID for a <a href="/windows-hardware/drivers/install/overview-of-device-setup-classes">device setup class</a> or a <a href="/windows-hardware/drivers/install/overview-of-device-interface-classes">device interface class</a>. This pointer is optional and can be <b>NULL</b>. If a GUID value is not used to select devices, set <i>ClassGuid</i> to <b>NULL</b>. For more information about how to use <i>ClassGuid</i>, see the following <b>Remarks</b> section.

### -param Enumerator [in, optional]

A pointer to a NULL-terminated string that specifies:

<ul>
<li>
An identifier (ID) of a Plug and Play (PnP) <a href="/windows-hardware/drivers/">enumerator</a>. This ID can either be the enumerator's globally unique identifier (GUID) or symbolic name. For example, "PCI" can be used to specify the PCI PnP enumerator. Other examples of symbolic names for PnP enumerators include "USB", "PCMCIA", and "SCSI".

</li>
<li>
 A PnP <a href="/windows-hardware/drivers/install/device-instance-ids">device instance IDs</a>. When specifying a PnP device instance ID, DIGCF_DEVICEINTERFACE must be set in the Flags parameter.

</li>
</ul>
This pointer is optional and can be <b>NULL</b>. If an <i>Enumerator</i> value is not used to select devices, set <i>Enumerator</i> to <b>NULL</b>

For more information about how to set the <i>Enumerator</i> value, see the following <b>Remarks</b> section.

### -param hwndParent [in, optional]

A handle to the top-level window to be used for a user interface that is associated with installing a device instance in the device information set. This handle is optional and can be <b>NULL</b>.

### -param Flags [in]

A variable of type DWORD that specifies control options that filter the device information elements that are added to the device information set. This parameter can be a bitwise OR of one or more of the following flags. For more information about combining these control options, see the following <b>Remarks</b> section. 





#### DIGCF_ALLCLASSES

Return a list of installed devices for the specified device setup classes or device interface classes. 



#### DIGCF_DEVICEINTERFACE

Return devices that support device interfaces for the specified device interface classes. This flag must be set in the <i>Flags</i> parameter if the <i>Enumerator</i> parameter specifies a <a href="/windows-hardware/drivers/install/device-instance-ids">device instance ID</a>.



#### DIGCF_DEFAULT

Return only the device that is associated with the system default device interface, if one is set, for the specified device interface classes. 



#### DIGCF_PRESENT

Return only devices that are currently present. 



#### DIGCF_PROFILE

Return only devices that are a part of the current hardware profile.

### -param DeviceInfoSet [in, optional]

The handle to an existing <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> to which <b>SetupDiGetClassDevsEx</b> adds the requested device information elements. This parameter is optional and can be set to <b>NULL</b>. For more information about using this parameter, see the following <b>Remarks</b> section.

### -param MachineName [in, optional]

A pointer to a constant string that contains the name of a remote computer on which the devices reside. A value of <b>NULL</b> for <i>MachineName</i> specifies that the device is installed on the local computer. Remote computer is not supported beginning with Windows 8 and Windows Server 2012.

> [!CAUTION]
> Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.

### -param Reserved

Reserved for internal use. This parameter must be set to <b>NULL</b>.


##### - Flags.DIGCF_ALLCLASSES

Return a list of installed devices for the specified device setup classes or device interface classes. 


##### - Flags.DIGCF_DEFAULT

Return only the device that is associated with the system default device interface, if one is set, for the specified device interface classes. 


##### - Flags.DIGCF_DEVICEINTERFACE

Return devices that support device interfaces for the specified device interface classes. This flag must be set in the <i>Flags</i> parameter if the <i>Enumerator</i> parameter specifies a <a href="/windows-hardware/drivers/install/device-instance-ids">device instance ID</a>.


##### - Flags.DIGCF_PRESENT

Return only devices that are currently present. 


##### - Flags.DIGCF_PROFILE

Return only devices that are a part of the current hardware profile.

## -returns

If the operation succeeds, <b>SetupDiGetClassDevsEx</b> returns a handle to a <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains all installed devices that matched the supplied parameters. If the operation fails, the function returns INVALID_HANDLE_VALUE. To get extended error information, call <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The caller of <b>SetupDiGetClassDevsEx</b> must delete the returned device information set when it is no longer needed by calling <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist">SetupDiDestroyDeviceInfoList</a>. 

If <i>DeviceInfoSet</i> is <b>NULL</b>, <b>SetupDiGetClassDevsEx</b> creates a new device information set that contains the retrieved device information elements and returns a handle to the new device information set. If the caller requests that the function retrieve devices for a device setup class that is supplied by the <i>ClassGuid </i> parameter, the function sets the device setup class of the new device information set to the supplied class GUID.  

If <i>DeviceInfoSet</i> is not set to <b>NULL</b>, the function adds the retrieved device information elements to the device information set that is associated with the supplied handle, and returns the supplied handle. If <i>ClassGuid</i> supplies a device setup class, the device setup class of the supplied device information set must be set to the supplied class GUID. 

<h3><a id="device_setup_class_control_options"></a><a id="DEVICE_SETUP_CLASS_CONTROL_OPTIONS"></a>Device Setup Class Control Options</h3>
Use the following filtering options to control whether <b>SetupDiGetClassDevsEx</b> returns devices for all device setup classes or only for a specified device setup class:

<ul>
<li>
To return devices for all device setup classes, set the DIGCF_ALLCLASSES flag and set the <i>ClassGuid</i> parameter to <b>NULL</b>.

</li>
<li>
To return devices only for a specific device setup class, do not set DIGCF_ALLCLASSES and use <i>ClassGuid</i> to supply the GUID of the device setup class.

</li>
</ul>
In addition, you can use the following filtering options to further restrict which devices are returned. 

<ul>
<li>
To return only devices that are present in the system, set the DIGCF_PRESENT flag. 

</li>
<li>
To return only devices that are part of the current hardware profile, set the DIGCF_PROFILE flag. 

</li>
<li>
To return devices for a specific PnP <a href="/windows-hardware/drivers/">enumerator</a> only, use the <i>Enumerator</i> parameter to supply the GUID or symbolic name of the enumerator<i>. </i>If <i>Enumerator</i> is <b>NULL</b>, <b>SetupDiGetClassDevsEx</b> returns devices for all PnP enumerators.

</li>
</ul>
<h3><a id="device_interface_class_control_options"></a><a id="DEVICE_INTERFACE_CLASS_CONTROL_OPTIONS"></a>Device Interface Class Control Options</h3>
Use the following filtering options to control whether <b>SetupDiGetClassDevsEx</b> returns devices that support any device interface class or only devices that support a specified device interface class:

<ul>
<li>
To return devices that support a device interface of any class, set the DIGCF_DEVICEINTERFACE flag, set the DIGCF_ALLCLASSES flag, and set <i>ClassGuid</i> to <b>NULL</b>. The function adds to the device information set a device information element that represents such a device, and then adds to the device information element a device interface list that contains all the device interfaces that the device supports.

</li>
<li>
To return only devices that support a device interface of a specified class, set the DIGCF_DEVICEINTERFACE flag and use the <i>ClassGuid</i> parameter to supply the class GUID of the device interface class. The function adds to the device information set a device information element that represents such a device, and then adds a device interface of the specified class to the device interface list for that device information element.

</li>
</ul>
In addition, you can use the following filtering options to control whether <b>SetupDiGetClassDevsEx</b> returns only devices that support the system default interface for device interface classes:

<ul>
<li>
To return only the device that supports the system default interface, if one is set, for a specified device interface class, set the DIGCF_DEVICEINTERFACE flag, set the DIGCF_DEFAULT flag, and use <i>ClassGuid</i> to supply the class GUID of the device interface class. The function adds to the device information set a device information element that represents such a device, and then adds the system default interface to the device interface list for that device information element. 

</li>
<li>
To return a device that supports a system default interface for an unspecified device interface class, set the DIGCF_DEVICEINTERFACE flag, set the DIGCF_ALLCLASSES flag, set the DIGCF_DEFAULT flag, and set <i>ClassGuid</i> to <b>NULL</b>. The function adds to the device information set a device information element that represents such a device, and then adds the system default interface to the device interface list for that device information element. 

</li>
</ul>
You can also use the following options in combination with the other options to further restrict which devices are returned. 

<ul>
<li>
To return only devices that are present in the system, set the DIGCF_PRESENT flag. 

</li>
<li>
To return only devices that are part of the current hardware profile, set the DIGCF_PROFILE flag. 

</li>
<li>
To return only a specific device, set the DIGCF_DEVICEINTERFACE flag and use the <i>Enumerator</i> parameter to supply the <a href="/windows-hardware/drivers/install/device-instance-ids">device instance ID</a> of the device<i>. </i>To include all possible devices, set <i>Enumerator</i> to <b>NULL</b>.

</li>
</ul>
<h3><a id="retrieving_devices_in_a_device_setup_class_that_support_a_device_inter"></a><a id="RETRIEVING_DEVICES_IN_A_DEVICE_SETUP_CLASS_THAT_SUPPORT_A_DEVICE_INTER"></a>Retrieving Devices in a Device Setup Class That Support a Device Interface Class</h3>
An installer can use <b>SetupDiGetClassDevsEx</b> to retrieve a list of devices of a particular device setup class that support a device interface of a specified device interface class. For example, to retrieve a list of all devices on a local computer that support a device interface in the "mounted device" interface class and that are members of the "Volume" device setup class, an installer should perform the following operations:

<ol>
<li>
Call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicreatedeviceinfolistexa">SetupDiCreateDeviceInfoList</a> to create an empty device information set for the "Volume" device setup class. Set <i>ClassGuid</i> to a pointer to the class GUID for the "Volume" device setup class and set <i>hwndParent</i> as appropriate. In response to such a call, the function will return a handle to type HDEVINFO to the device information set.

</li>
<li>Call <b>SetupDiGetClassDevsEx</b> with the following settings:<ul>
<li>Set <i>ClassGuid</i> to a pointer to the class GUID of the "mounted device" device interface class.</li>
<li>Set <i>Flags</i> to DIGCF_DEVICEINTERFACE.</li>
<li>Set <i>DeviceInfoSet</i> to the HDEVINFO handle obtained in step (1).</li>
<li>Set <i>hwndParent</i> as appropriate and the remaining parameters to <b>NULL</b>.</li>
</ul>
</li>
</ol>
In an operation of this type, <b>SetupDiGetClassDevsEx</b> returns a device if the device setup class of the device is the same as the supplied device information set and if the device supports a device interface whose class is the same as the specified device interface class.





> [!NOTE]
> The setupapi.h header defines SetupDiGetClassDevsEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows-hardware/drivers/install/device-information-sets">Device Information Set</a>



<a href="/windows-hardware/drivers/install/device-instance-ids">Device Instance IDs</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicreatedeviceinfolistexa">SetupDiCreateDeviceInfoListEx</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist">SetupDiDestroyDeviceInfoList</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces">SetupDiEnumDeviceInterfaces</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassdevsw">SetupDiGetClassDevs</a>
