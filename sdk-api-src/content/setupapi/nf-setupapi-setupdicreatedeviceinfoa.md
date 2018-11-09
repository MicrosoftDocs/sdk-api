---
UID: NF:setupapi.SetupDiCreateDeviceInfoA
title: SetupDiCreateDeviceInfoA function
author: windows-sdk-content
description: The SetupDiCreateDeviceInfo function creates a new device information element and adds it as a new member to the specified device information set.
old-location: devinst\setupdicreatedeviceinfo.htm
tech.root: devinst
ms.assetid: 7d42167f-9af4-4aee-b641-a93ade1e3969
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: SetupDiCreateDeviceInfo, SetupDiCreateDeviceInfo function [Device and Driver Installation], SetupDiCreateDeviceInfoA, SetupDiCreateDeviceInfoW, devinst.setupdicreatedeviceinfo, di-rtns_a4c64729-99b8-44d0-a404-1def9567bf33.xml, setupapi/SetupDiCreateDeviceInfo
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
 - SetupDiCreateDeviceInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupDiCreateDeviceInfoA function


## -description


The <b>SetupDiCreateDeviceInfo</b> function creates a new device information element and adds it as a new member to the specified device information set.


## -parameters




### -param DeviceInfoSet [in]

A handle to the <a href="https://msdn.microsoft.com/library/Ff541247(v=VS.85).aspx">device information set</a> for the local computer.


### -param DeviceName [in]

A pointer to a NULL-terminated string that supplies either a full <a href="https://msdn.microsoft.com/library/Ff541327(v=VS.85).aspx">device instance ID</a> (for example, "Root\*PNP0500\0000") or a root-enumerated <a href="https://msdn.microsoft.com/library/Ff541237(v=VS.85).aspx">device ID</a> without the enumerator prefix and instance identifier suffix (for example, "*PNP0500"). The root-enumerated device identifier can be used only if the DICD_GENERATE_ID flag is specified in the <i>CreationFlags</i> parameter.


### -param ClassGuid [in]

A pointer to the <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff552344">device setup class</a> GUID for the device. If the device setup class of the device is not known, set *<i>ClassGuid</i> to a GUID_NULL structure. 


### -param DeviceDescription [in, optional]

A pointer to a NULL-terminated string that supplies the text description of the device. This pointer is optional and can be <b>NULL</b>.


### -param hwndParent [in, optional]

A handle to the top-level window to use for any user interface that is related to installing the device. This handle is optional and can be <b>NULL</b>.


### -param CreationFlags [in]

A variable of type DWORD that controls how the device information element is created. Can be a combination of the following values:





#### DICD_GENERATE_ID

If this flag is specified, <i>DeviceName</i> contains only a Root-enumerated <a href="https://msdn.microsoft.com/library/Ff541237(v=VS.85).aspx">device ID</a> and the system uses that ID to generate a full <a href="https://msdn.microsoft.com/library/Ff541327(v=VS.85).aspx">device instance ID</a> for the new device information element.

Call <b>SetupDiGetDeviceInstanceId</b> to retrieve the device instance ID that was generated for this device information element.



#### DICD_INHERIT_CLASSDRVS

If this flag is specified, the resulting device information element inherits the class driver list, if any, associated with the device information set. In addition, if there is a selected driver for the device information set, that same driver is selected for the new device information element.


### -param DeviceInfoData [out, optional]

A pointer to a <a href="https://msdn.microsoft.com/9ad0ef4f-4a67-4f16-8bb1-2242dad0d041">SP_DEVINFO_DATA</a> structure that receives the new device information element. This pointer is optional and can be <b>NULL</b>. If the structure is supplied, the caller must set the <b>cbSize</b> member of this structure to <b>sizeof(</b>SP_DEVINFO_DATA<b>)</b> before calling the function. For more information, see the following <b>Remarks</b> section. 


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by making a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



The caller of this function must be a member of the Administrators group.

If this device instance is being added to a set that has an associated class, the device class must be the same or the call fails. In this case, a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a> returns ERROR_CLASS_MISMATCH.

If the specified device instance is the same as an existing device instance key in the registry, the call fails. In this case, a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a> returns ERROR_DEVINST_ALREADY_EXISTS. This occurs only if the DICD_GENERATE_ID flag is not set.

If the new device information element was successfully created but the caller-supplied <i>DeviceInfoData</i> buffer is invalid, the function returns <b>FALSE</b>. In this case, a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a> returns ERROR_INVALID_USER_BUFFER. However, the device information element will have been added as a new member of the set already.

The <i>DeviceInfoSet</i> must only contain elements on the local computer.




## -see-also




<a href="https://msdn.microsoft.com/9ad0ef4f-4a67-4f16-8bb1-2242dad0d041">SP_DEVINFO_DATA</a>



<a href="https://msdn.microsoft.com/f510c42d-8488-4aad-a3a4-662fc8138d28">SetupDiDeleteDeviceInfo</a>



<a href="https://msdn.microsoft.com/34df0557-eb86-4b00-bbd7-a4f0c1b82ff4">SetupDiEnumDeviceInfo</a>



<a href="https://msdn.microsoft.com/0c4a2d09-62b2-43ce-a202-aeb59248d9fc">SetupDiOpenDeviceInfo</a>
 

 

