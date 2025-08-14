---
UID: NF:setupapi.SetupDiGetClassDevsW
title: SetupDiGetClassDevsW function (setupapi.h)
description: The SetupDiGetClassDevs function returns a handle to a device information set that contains requested device information elements for a local computer. (Unicode)
helpviewer_keywords: ["SetupDiGetClassDevs", "SetupDiGetClassDevs function [Device and Driver Installation]", "SetupDiGetClassDevsW", "devinst.setupdigetclassdevs", "di-rtns_8f48a4a7-e4b9-4843-aacc-88f678b4145c.xml", "setupapi/SetupDiGetClassDevs", "setupapi/SetupDiGetClassDevsW"]
old-location: devinst\setupdigetclassdevs.htm
tech.root: devinst
ms.assetid: 31bb0fc8-0fb8-4122-b9e8-5ff8fbbd903b
ms.date: 12/05/2018
ms.keywords: SetupDiGetClassDevs, SetupDiGetClassDevs function [Device and Driver Installation], SetupDiGetClassDevsW, devinst.setupdigetclassdevs, di-rtns_8f48a4a7-e4b9-4843-aacc-88f678b4145c.xml, setupapi/SetupDiGetClassDevs, setupapi/SetupDiGetClassDevsW
req.header: setupapi.h
req.include-header: SetupAPI.h
req.target-type: DesktopFor universal, call CM_Get_Device_ID_ListFor universal, call CM_Get_Device_Interface_List
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupDiGetClassDevsW (Unicode)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: SetupAPI.lib
req.dll: SetupAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupDiGetClassDevsW
 - setupapi/SetupDiGetClassDevsW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-setupapi-devobj-l1-1-0.dll
 - SetupAPI.dll
 - ext-ms-win-setupapi-classinstallers-l1-1-0.dll
 - Ext-MS-Win-SetupAPI-ClassInstallers-L1-1-1.dll
 - Ext-MS-Win-SetupAPI-ClassInstallers-L1-1-2.dll
api_name:
 - SetupDiGetClassDevs
 - SetupDiGetClassDevsW
req.apiset: ext-ms-win-setupapi-classinstallers-l1-1-0 (introduced in Windows 8)
---

# SetupDiGetClassDevsW function


## -description

The <b>SetupDiGetClassDevs</b> function returns a handle to a <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains requested device information elements for a local computer.

## -parameters

### -param ClassGuid [in, optional]

A pointer to the GUID for a <a href="/windows-hardware/drivers/install/overview-of-device-setup-classes">device setup class</a> or a <a href="/windows-hardware/drivers/install/overview-of-device-interface-classes">device interface class</a>. This pointer is optional and can be <b>NULL</b>. For more information about how to set <i>ClassGuid</i>, see the following <b>Remarks</b> section.

### -param Enumerator [in, optional]

A pointer to a NULL-terminated string that specifies:

<ul>
<li>
An identifier (ID) of a Plug and Play (PnP) <a href="/windows-hardware/drivers/">enumerator</a>. This ID can either be the value's globally unique identifier (GUID) or symbolic name. For example, "PCI" can be used to specify the PCI PnP value. Other examples of symbolic names for PnP values include "USB," "PCMCIA," and "SCSI".

</li>
<li>
A PnP <a href="/windows-hardware/drivers/install/device-instance-ids">device instance ID</a>. When specifying a PnP device instance ID, DIGCF_DEVICEINTERFACE must be set in the Flags parameter.

</li>
</ul>
This pointer is optional and can be <b>NULL</b>. If an <i>enumeration</i> value is not used to select devices, set <i>Enumerator</i> to <b>NULL</b>

For more information about how to set the <i>Enumerator</i> value, see the following <b>Remarks</b> section.

### -param hwndParent [in, optional]

A handle to the top-level window to be used for a user interface that is associated with installing a device instance in the device information set. This handle is optional and can be <b>NULL</b>.

### -param Flags [in]

A variable of type DWORD that specifies control options that filter the device information elements that are added to the device information set. This parameter can be a bitwise OR of zero or more of the following flags. For more information about combining these flags, see the following <b>Remarks</b> section. 





#### DIGCF_ALLCLASSES

Return a list of installed devices for all device setup classes or all device interface classes.



#### DIGCF_DEVICEINTERFACE

Return devices that support device interfaces for the specified device interface classes. This flag must be set in the <i>Flags</i> parameter if the <i>Enumerator</i> parameter specifies a <a href="/windows-hardware/drivers/install/device-instance-ids">device instance ID</a>.



#### DIGCF_DEFAULT

Return only the device that is associated with the system default device interface, if one is set, for the specified device interface classes.



#### DIGCF_PRESENT

Return only devices that are currently present in a system.



#### DIGCF_PROFILE

Return only devices that are a part of the current hardware profile.

## -returns

If the operation succeeds, <b>SetupDiGetClassDevs</b> returns a handle to a <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains all installed devices that matched the supplied parameters. If the operation fails, the function returns INVALID_HANDLE_VALUE. To get extended error information, call <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The caller of <b>SetupDiGetClassDevs</b> must delete the returned device information set when it is no longer needed by calling <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist">SetupDiDestroyDeviceInfoList</a>.

Call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassdevsexa">SetupDiGetClassDevsEx</a> to retrieve the devices for a class on a remote computer.

<h3><a id="device_setup_class_control_options"></a><a id="DEVICE_SETUP_CLASS_CONTROL_OPTIONS"></a>Device Setup Class Control Options</h3>
Use the following filtering options to control whether <b>SetupDiGetClassDevs</b> returns devices for all device setup classes or only for a specified device setup class:

<ul>
<li>
To return devices for all device setup classes, set the DIGCF_ALLCLASSES flag, and set the <i>ClassGuid</i> parameter to <b>NULL</b>.

</li>
<li>
To return devices only for a specific device setup class, do not set DIGCF_ALLCLASSES, and use <i>ClassGuid</i> to supply the GUID of the device setup class.

</li>
</ul>
In addition, you can use the following filtering options in combination with one another to further restrict which devices are returned:

<ul>
<li>
To return only devices that are present in the system, set the DIGCF_PRESENT flag.

</li>
<li>
To return only devices that are part of the current hardware profile, set the DIGCF_PROFILE flag.

</li>
<li>
To return devices only for a specific PnP <a href="/windows-hardware/drivers/">enumerator</a>, use the <i>Enumerator</i> parameter to supply the GUID or symbolic name of the enumerator<i>. </i>If <i>Enumerator</i> is <b>NULL</b>, <b>SetupDiGetClassDevs</b> returns devices for all PnP enumerators.

</li>
</ul>
<h3><a id="device_interface_class_control_options"></a><a id="DEVICE_INTERFACE_CLASS_CONTROL_OPTIONS"></a>Device Interface Class Control Options</h3>
Use the following filtering options to control whether <b>SetupDiGetClassDevs</b> returns devices that support any device interface class or only devices that support a specified device interface class:

<ul>
<li>
To return devices that support a device interface of any class, set the DIGCF_DEVICEINTERFACE flag, set the DIGCF_ALLCLASSES flag, and set <i>ClassGuid</i> to <b>NULL</b>. The function adds to the device information set a device information element that represents such a device and then adds to the device information element a device interface list that contains all the device interfaces that the device supports.

</li>
<li>
To return only devices that support a device interface of a specified class, set the DIGCF_DEVICEINTERFACE flag and use the <i>ClassGuid</i> parameter to supply the class GUID of the device interface class. The function adds to the device information set a device information element that represents such a device and then adds a device interface of the specified class to the device interface list for that device information element.

</li>
</ul>
In addition, you can use the following filtering options to control whether <b>SetupDiGetClassDevs</b> returns only devices that support the system default interface for device interface classes:

<ul>
<li>
To return only the device that supports the system default interface, if one is set, for a specified device interface class, set the DIGCF_DEVICEINTERFACE flag, set the DIGCF_DEFAULT flag, and use <i>ClassGuid</i> to supply the class GUID of the device interface class. The function adds to the device information set a device information element that represents such a device and then adds the system default interface to the device interface list for that device information element.

</li>
<li>
To return a device that supports a system default interface for an unspecified device interface class, set the DIGCF_DEVICEINTERFACE flag, set the DIGCF_ALLCLASSES flag, set the DIGCF_DEFAULT flag, and set <i>ClassGuid</i> to <b>NULL</b>. The function adds to the device information set a device information element that represents such a device and then adds the system default interface to the device interface list for that device information element.

</li>
</ul>
You can also use the following options in combination with the other options to further restrict which devices are returned:

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

#### Examples

The following are some examples of how to use the <b>SetupDiGetClassDevs</b> function.

<b>Example 1: </b>Build a list of all devices in the system, including devices that are not currently present.


```
Handle = SetupDiGetClassDevs(NULL, NULL, NULL, DIGCF_ALLCLASSES);
```


<b>Example 2: </b> Build a list of all devices that are present in the system.


```
Handle = SetupDiGetClassDevs(NULL, NULL, NULL, DIGCF_ALLCLASSES | DIGCF_PRESENT);
```


<b>Example 3: </b> Build a list of all devices that are present in the system that are from the network adapter <a href="/windows-hardware/drivers/install/system-defined-device-setup-classes-available-to-vendors">device setup class</a>.


```
Handle = SetupDiGetClassDevs(&GUID_DEVCLASS_NET, NULL, NULL, DIGCF_PRESENT);
```


<b>Example 4: </b> Build a list of all devices that are present in the system that have enabled an interface from the storage volume <a href="/windows-hardware/drivers/install/overview-of-device-interface-classes">device interface class</a>.


```
Handle = SetupDiGetClassDevs(&GUID_DEVINTERFACE_VOLUME, NULL, NULL, DIGCF_PRESENT | DIGCF_DEVICEINTERFACE);
```


<b>Example 5: </b> Build a list of all devices that are present in the system but do not belong to any known <a href="/windows-hardware/drivers/install/system-defined-device-setup-classes-available-to-vendors">device setup class</a> (Windows Vista and later versions of Windows).

<div class="alert"><b>Note</b>  You cannot set the <i>ClassGuid</i> parameter to GUID_DEVCLASS_UNKNOWN to detect devices with an unknown setup class. Instead, you must follow this example.</div>
<div> </div>

```
HDEVINFO DeviceInfoSet = SetupDiGetClassDevs(
                                    NULL,
                                    NULL,
                                    NULL,
                                    DIGCF_ALLCLASSES | DIGCF_PRESENT);

SP_DEVINFO_DATA DeviceInfoData;
ZeroMemory(&DeviceInfoData, sizeof(SP_DEVINFO_DATA));
DeviceInfoData.cbSize = sizeof(SP_DEVINFO_DATA);
DWORD DeviceIndex = 0;
    
while (SetupDiEnumDeviceInfo(
                             DeviceInfoSet,
                             DeviceIndex,
                             &DeviceInfoData)) {
    DeviceIndex++;

    if (!SetupDiGetDeviceProperty(
                                  DeviceInfoSet,
                                  &DeviceInfoData,
                                  &DEVPKEY_Device_Class,
                                  &PropType,
                                  (PBYTE)&DevGuid,
                                  sizeof(GUID),
                                  &Size,
                                  0) || PropType != DEVPROP_TYPE_GUID) {

        Error = GetLastError();

        if (Error == ERROR_NOT_FOUND) {
            //
            // This device has an unknown device setup class.
            //
        }
    }                 
}

if (DeviceInfoSet) {
    SetupDiDestroyDeviceInfoList(DeviceInfoSet);
}
```






> [!NOTE]
> The setupapi.h header defines SetupDiGetClassDevs as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows-hardware/drivers/install/device-information-sets">Device Information Set</a>



<a href="/windows-hardware/drivers/install/device-instance-ids">Device Instance IDs</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicreatedeviceinfolist">SetupDiCreateDeviceInfoList</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist">SetupDiDestroyDeviceInfoList</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces">SetupDiEnumDeviceInterfaces</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassdevsexa">SetupDiGetClassDevsEx</a>
