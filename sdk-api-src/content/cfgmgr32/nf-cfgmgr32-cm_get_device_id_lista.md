---
UID: NF:cfgmgr32.CM_Get_Device_ID_ListA
title: CM_Get_Device_ID_ListA function (cfgmgr32.h)
description: The CM_Get_Device_ID_List function retrieves a list of device instance IDs for the local computer's device instances. (ANSI)
helpviewer_keywords: ["CM_Get_Device_ID_ListA", "cfgmgr32/CM_Get_Device_ID_ListA", "cfgmgrfn_e9f614d2-9bac-4b30-b9a0-f0764e37950b.xml"]
old-location: devinst\cm_get_device_id_list.htm
tech.root: devinst
ms.assetid: aa0ab004-3813-4339-90bb-afd9acf200c8
ms.date: 12/05/2018
ms.keywords: CM_Get_Device_ID_List, CM_Get_Device_ID_List function [Device and Driver Installation], CM_Get_Device_ID_ListA, CM_Get_Device_ID_ListW, cfgmgr32/CM_Get_Device_ID_List, cfgmgr32/CM_Get_Device_ID_ListA, cfgmgr32/CM_Get_Device_ID_ListW, cfgmgrfn_e9f614d2-9bac-4b30-b9a0-f0764e37950b.xml, devinst.cm_get_device_id_list
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Universal
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CM_Get_Device_ID_ListW (Unicode) and CM_Get_Device_ID_ListA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Cfgmgr32.lib
req.dll: CfgMgr32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CM_Get_Device_ID_ListA
 - cfgmgr32/CM_Get_Device_ID_ListA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-devices-config-l1-1-2.dll
 - CfgMgr32.dll
 - API-MS-Win-Devices-Config-L1-1-0.dll
 - API-MS-Win-Devices-Config-L1-1-1.dll
api_name:
 - CM_Get_Device_ID_List
 - CM_Get_Device_ID_ListA
 - CM_Get_Device_ID_ListW
---

# CM_Get_Device_ID_ListA function


## -description

The <b>CM_Get_Device_ID_List</b> function retrieves a list of <a href="/windows-hardware/drivers/install/device-instance-ids">device instance IDs</a> for the local computer's <a href="/windows-hardware/drivers/">device instances</a>.

## -parameters

### -param pszFilter [in, optional]

Caller-supplied pointer to a character string that is either set to a subset of the computer's device instance identifiers (IDs), or to <b>NULL</b>. See the following description of <i>ulFlags</i>.

### -param Buffer [out]

Address of a buffer to receive a set of NULL-terminated device instance identifier strings. The end of the set is terminated by an extra <b>NULL</b>. The required buffer size should be obtained by calling <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_sizea">CM_Get_Device_ID_List_Size</a>.

### -param BufferLen [in]

Caller-supplied length, in characters, of the buffer specified by <i>Buffer</i>.

### -param ulFlags [in]

One of the following caller-supplied bit flags that specifies search filters:





#### CM_GETIDLIST_FILTER_BUSRELATIONS

If this flag is set, <i>pszFilter</i> must specify a device instance identifier. The function returns device instance IDs for the <a href="/windows-hardware/drivers/kernel/irp-mn-query-device-relations">bus relations</a> of the specified device instance.



#### CM_GETIDLIST_FILTER_CLASS (Windows 7 and later versions of Windows)

If this flag is set, <i>pszFilter</i> contains a string that specifies a <a href="/windows-hardware/drivers/install/overview-of-device-setup-classes">device setup class</a> GUID. The returned list contains device instances for which the property (referenced by the CM_DRP_CLASSGUID constant) matches the specified device setup class GUID. 

The CM_DRP_CLASSGUID constant is defined in <i>Cfgmgr32.h</i>.



#### CM_GETIDLIST_FILTER_PRESENT (Windows 7 and later versions of Windows)

If this flag is set, the returned list contains only device instances that are currently present on the system. This value can be combined with other <i>ulFlags</i> values, such as CM_GETIDLIST_FILTER_CLASS.



#### CM_GETIDLIST_FILTER_TRANSPORTRELATIONS (Windows 7 and later versions of Windows)

If this flag is set, <i>pszFilter</i> must specify the device instance identifier of a composite device node (<a href="/windows-hardware/drivers/">devnode</a>).

The function returns the device instance identifiers of the devnodes that represent the transport relations of the specified composite devnode. 

For more information about composite devnodes and transport relations, see the following <b>Remarks</b> section.



#### CM_GETIDLIST_DONOTGENERATE

Used only with CM_GETIDLIST_FILTER_SERVICE. If set, and if the device tree does not contain a devnode for the specified service, this flag prevents the function from creating a devnode for the service. 



#### CM_GETIDLIST_FILTER_EJECTRELATIONS

If this flag is set, <i>pszFilter</i> must specify a device instance identifier. The function returns device instance IDs for the <a href="/windows-hardware/drivers/kernel/irp-mn-query-device-relations">ejection relations</a> of the specified device instance.



#### CM_GETIDLIST_FILTER_ENUMERATOR

If this flag is set, *pszFilter* must specify the name of a device enumerator, optionally followed by a <a href="/windows-hardware/drivers/install/device-ids">device ID</a>. The string format is *EnumeratorName*\\&lt;*DeviceID*&gt;, such as **ROOT** or **ROOT\\\*PNP0500**.

If <i>pszFilter</i> supplies only an enumerator name, the function returns <a href="/windows-hardware/drivers/install/device-instance-ids">device instance IDs</a> for the instances of each device associated with the enumerator. Enumerator names can be obtained by calling <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_enumerate_enumeratorsw">CM_Enumerate_Enumerators</a>.

If <i>pszFilter</i> supplies both an enumerator and a <a href="/windows-hardware/drivers/install/device-ids">device ID</a>, the function returns <a href="/windows-hardware/drivers/install/device-instance-ids">device instance IDs</a> only for the instances of the specified device that is associated with the enumerator.



#### CM_GETIDLIST_FILTER_NONE

If this flag is set, <i>pszFilter</i> is ignored, and a list of all devices on the system is returned.



#### CM_GETIDLIST_FILTER_POWERRELATIONS

If this flag is set, <i>pszFilter</i> must specify a device instance identifier. The function returns device instance IDs for the power relations of the specified device instance.



#### CM_GETIDLIST_FILTER_REMOVALRELATIONS

If this flag is set, <i>pszFilter</i> must specify a device instance identifier. The function returns device instance IDs for the <a href="/windows-hardware/drivers/kernel/irp-mn-query-device-relations">removal relations</a> of the specified device instance.



#### CM_GETIDLIST_FILTER_SERVICE

If this flag is set, <i>pszFilter</i> must specify the name of a Microsoft Windows service (typically a driver). The function returns device instance IDs for the device instances controlled by the specified service.

Note that if the device tree does not contain a <a href="/windows-hardware/drivers/">devnode</a> for the specified service, this function creates one by default. To inhibit this behavior, also set CM_GETIDLIST_DONOTGENERATE.

If no search filter flag is specified, the function returns all device instance IDs for all device instances.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

## -remarks

Starting with Windows 7, a device that supports multiple transport paths for packet-based data is referred to as a <i>composite </i> device and is represented by a <i>composite </i><a href="/windows-hardware/drivers/">devnode</a>. A composite devnode logically represents the composite device to the user and applications as a single device, even though the composite devnode can have multiple paths to the physical device. 

Each active transport path to the physical device is represented by a transport devnode and is referred to as a <i>transport relation</i> for the composite device.

The composite devnode (but not the related transport devnodes) exposes device interfaces to applications and the system. When an application uses these public device interfaces, the composite device routes the packet-based data to one or more of these transport devnodes, which then transport the data to the physical device.

For example, if a physical cell phone is simultaneously connected to the computer on the USB and the Bluetooth buses, each bus enumerates a child transport devnode on that bus to represent the device's physical connection. 

In this case, if you set the CM_GETIDLIST_FILTER_TRANSPORTRELATIONS flags in <i>ulFlags</i> and specify the device instance ID of the cell phone's composite devnode in <i>pszFilter</i>, the function returns the device instance IDs for the two transport devnodes in the <i>Buffer</i> parameter.

For more information about device instance IDs, see <a href="/windows-hardware/drivers/install/device-identification-strings">Device Identification Strings</a>.





> [!NOTE]
> The cfgmgr32.h header defines CM_Get_Device_ID_List as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_sizea">CM_Get_Device_ID_List_Size</a>
