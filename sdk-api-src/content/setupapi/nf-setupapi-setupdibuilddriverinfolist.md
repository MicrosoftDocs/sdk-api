---
UID: NF:setupapi.SetupDiBuildDriverInfoList
title: SetupDiBuildDriverInfoList function
author: windows-sdk-content
description: The SetupDiBuildDriverInfoList function builds a list of drivers that is associated with a specific device or with the global class driver list for a device information set.
old-location: devinst\setupdibuilddriverinfolist.htm
tech.root: devinst
ms.assetid: 9e377865-8029-41c1-85b9-fdb2cbc09346
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: SPDIT_CLASSDRIVER, SPDIT_COMPATDRIVER, SetupDiBuildDriverInfoList, SetupDiBuildDriverInfoList function [Device and Driver Installation], devinst.setupdibuilddriverinfolist, di-rtns_dd9aa1be-1a67-4cc6-8a06-5db71eecd322.xml, setupapi/SetupDiBuildDriverInfoList
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupDiBuildDriverInfoList function


## -description


The <b>SetupDiBuildDriverInfoList</b> function builds a list of drivers that is associated with a specific device or with the global class driver list for a device information set. 


## -parameters




### -param DeviceInfoSet [in]

A handle to the <a href="devinst.device_information_sets">device information set</a> to contain the driver list, either globally for all device information elements or specifically for a single device information element. The device information set must not contain remote device information elements.


### -param DeviceInfoData [in, out]

A pointer to an <a href="https://msdn.microsoft.com/9ad0ef4f-4a67-4f16-8bb1-2242dad0d041">SP_DEVINFO_DATA</a> structure for the device information element in <i>DeviceInfoSet</i> that represents the device for which to build a driver list. This parameter is optional and can be <b>NULL</b>. If this parameter is specified, the list is associated with the specified device. If this parameter is <b>NULL</b>, the list is associated with the global class driver list for <i>DeviceInfoSet</i>. 

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



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by making a call to <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The device information set should be for a local computer because <b>SetupDiBuildDriverInfoList</b> searches for drivers only on a local computer. If the device information set is for a remote computer, the function returns <b>TRUE</b> but does not actually update the existing driver list for the device information set or, if supplied, the driver list for the device information element.

The caller can set <b>Flags</b> in the <a href="https://msdn.microsoft.com/1bd21150-f8f4-480d-a4b2-99fa4b4233b9">SP_DEVINSTALL_PARAMS</a> that are associated with the device information set or with a specific device (<i>DeviceInfoData</i>) to control how the list is built. For example, the caller can set the <b>DI_FLAGSEX_ALLOWEXCLUDEDDRVS</b> flag to include drivers that are marked Exclude From Select.

A driver is "Exclude From Select" if either it is marked <b>ExcludeFromSelect</b> in the INF file or it is a driver for a device whose whole setup class is marked <b>NoInstallClass</b> or <b>NoUseClass</b> in the class installer INF file. Drivers for PnP devices are typically "Exclude From Select"; PnP devices should not be manually installed. To build a list of driver files for a PnP device a caller of <b>SetupDiBuildDriverInfoList</b> must set this flag. 

The <b>DriverPath</b> in the <a href="https://msdn.microsoft.com/1bd21150-f8f4-480d-a4b2-99fa4b4233b9">SP_DEVINSTALL_PARAMS</a> contains either a path of a directory that contain INF files or a path of a specific INF file. If <b>DI_ENUMSINGLEINF</b> is set, <b>DriverPath</b> contains a path of a single INF file. If <b>DriverPath</b> is <b>NULL</b>, this function builds the driver list from the default INF file location, %SystemRoot%\inf. 

After this function has built the specified driver list, the caller can enumerate the elements of the list by calling <a href="https://msdn.microsoft.com/c4a66d0c-e9a9-41f8-87df-576795667b5c">SetupDiEnumDriverInfo</a>.

If the driver list is associated with a device instance (that is, <i>DeviceInfoData</i> is specified), the resulting list is composed of drivers that have the same class as the device instance with which they are associated. If this is a global class driver list (that is, <i>DriverType</i> is <b>SPDIT_CLASSDRIVER</b> and <i>DeviceInfoData</i> is not specified), the class that is used when building the list is the class associated with the device information set. If the device information set has no associated class, drivers of all classes are used when building the list.

Another thread can terminate the building of a driver list by a call to <a href="https://msdn.microsoft.com/847f1f5e-5634-44ea-b530-6136629f0471">SetupDiCancelDriverInfoSearch</a>.

The <i>DeviceInfoSet</i> must only contain elements on the local computer. This function only searches for local drivers.




## -see-also




<a href="https://msdn.microsoft.com/847f1f5e-5634-44ea-b530-6136629f0471">SetupDiCancelDriverInfoSearch</a>



<a href="https://msdn.microsoft.com/d8067609-1046-4641-9f57-b0ee2be5a3b2">SetupDiDestroyDriverInfoList</a>



<a href="https://msdn.microsoft.com/c4a66d0c-e9a9-41f8-87df-576795667b5c">SetupDiEnumDriverInfo</a>
 

 

