---
UID: NF:setupapi.SetupDiBuildDriverInfoList
title: SetupDiBuildDriverInfoList function (setupapi.h)
description: The SetupDiBuildDriverInfoList function builds a list of drivers that is associated with a specific device or with the global class driver list for a device information set.
helpviewer_keywords: ["SPDIT_CLASSDRIVER","SPDIT_COMPATDRIVER","SetupDiBuildDriverInfoList","SetupDiBuildDriverInfoList function [Device and Driver Installation]","devinst.setupdibuilddriverinfolist","di-rtns_dd9aa1be-1a67-4cc6-8a06-5db71eecd322.xml","setupapi/SetupDiBuildDriverInfoList"]
old-location: devinst\setupdibuilddriverinfolist.htm
tech.root: devinst
ms.assetid: 9e377865-8029-41c1-85b9-fdb2cbc09346
ms.date: 12/05/2018
ms.keywords: SPDIT_CLASSDRIVER, SPDIT_COMPATDRIVER, SetupDiBuildDriverInfoList, SetupDiBuildDriverInfoList function [Device and Driver Installation], devinst.setupdibuilddriverinfolist, di-rtns_dd9aa1be-1a67-4cc6-8a06-5db71eecd322.xml, setupapi/SetupDiBuildDriverInfoList
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
 - SetupDiBuildDriverInfoList
 - setupapi/SetupDiBuildDriverInfoList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
 - Ext-MS-Win-SetupAPI-ClassInstallers-l1-1-1.dll
 - Ext-MS-Win-SetupAPI-ClassInstallers-L1-1-2.dll
api_name:
 - SetupDiBuildDriverInfoList
req.apiset: ext-ms-win-setupapi-classinstallers-l1-1-1 (introduced in Windows 8.1)
---

# SetupDiBuildDriverInfoList function


## -description

The <b>SetupDiBuildDriverInfoList</b> function builds a list of drivers that is associated with a specific device or with the global class driver list for a device information set.

## -parameters

### -param DeviceInfoSet [in]

A handle to the <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> to contain the driver list, either globally for all device information elements or specifically for a single device information element. The device information set must not contain remote device information elements.

### -param DeviceInfoData [in, out]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure for the device information element in <i>DeviceInfoSet</i> that represents the device for which to build a driver list. This parameter is optional and can be <b>NULL</b>. If this parameter is specified, the list is associated with the specified device. If this parameter is <b>NULL</b>, the list is associated with the global class driver list for <i>DeviceInfoSet</i>. 

If the class of this device is updated because of building a compatible driver list, <i>DeviceInfoData.</i><b>ClassGuid</b> is updated upon return.

### -param DriverType [in]

The type of driver list to build. Must be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SPDIT_CLASSDRIVER"></a><a id="spdit_classdriver"></a><dl>
<dt><b>SPDIT_CLASSDRIVER</b></dt>
</dl>
</td>
<td width="60%">
Build a list of class drivers. If <i>DeviceInfoData</i> is <b>NULL</b>, this driver list type must be specified.

</td>
</tr>
<tr>
<td width="40%"><a id="SPDIT_COMPATDRIVER"></a><a id="spdit_compatdriver"></a><dl>
<dt><b>SPDIT_COMPATDRIVER</b></dt>
</dl>
</td>
<td width="60%">
Build a list of compatible drivers. <i>DeviceInfoData</i> must not be <b>NULL</b> if this driver list type is specified.

</td>
</tr>
</table>

## -returns

The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by making a call to <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The device information set should be for a local computer because <b>SetupDiBuildDriverInfoList</b> searches for drivers only on a local computer. If the device information set is for a remote computer, the function returns <b>TRUE</b> but does not actually update the existing driver list for the device information set or, if supplied, the driver list for the device information element.

The caller can set <b>Flags</b> in the <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinstall_params_a">SP_DEVINSTALL_PARAMS</a> that are associated with the device information set or with a specific device (<i>DeviceInfoData</i>) to control how the list is built. For example, the caller can set the <b>DI_FLAGSEX_ALLOWEXCLUDEDDRVS</b> flag to include drivers that are marked Exclude From Select.

A driver is "Exclude From Select" if either it is marked <b>ExcludeFromSelect</b> in the INF file or it is a driver for a device whose whole setup class is marked <b>NoInstallClass</b> or <b>NoUseClass</b> in the class installer INF file. Drivers for PnP devices are typically "Exclude From Select"; PnP devices should not be manually installed. To build a list of driver files for a PnP device a caller of <b>SetupDiBuildDriverInfoList</b> must set this flag. 

The <b>DriverPath</b> in the <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinstall_params_a">SP_DEVINSTALL_PARAMS</a> contains either a path of a directory that contain INF files or a path of a specific INF file. If <b>DI_ENUMSINGLEINF</b> is set, <b>DriverPath</b> contains a path of a single INF file. If <b>DriverPath</b> is <b>NULL</b>, this function builds the driver list from the default INF file location, %SystemRoot%\inf. 

After this function has built the specified driver list, the caller can enumerate the elements of the list by calling <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdienumdriverinfoa">SetupDiEnumDriverInfo</a>.

If the driver list is associated with a device instance (that is, <i>DeviceInfoData</i> is specified), the resulting list is composed of drivers that have the same class as the device instance with which they are associated. If this is a global class driver list (that is, <i>DriverType</i> is <b>SPDIT_CLASSDRIVER</b> and <i>DeviceInfoData</i> is not specified), the class that is used when building the list is the class associated with the device information set. If the device information set has no associated class, drivers of all classes are used when building the list.

Another thread can terminate the building of a driver list by a call to <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicanceldriverinfosearch">SetupDiCancelDriverInfoSearch</a>.

The <i>DeviceInfoSet</i> must only contain elements on the local computer. This function only searches for local drivers.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicanceldriverinfosearch">SetupDiCancelDriverInfoSearch</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdidestroydriverinfolist">SetupDiDestroyDriverInfoList</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdienumdriverinfoa">SetupDiEnumDriverInfo</a>
