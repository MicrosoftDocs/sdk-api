---
UID: NF:setupapi.SetupDiGetDeviceInstanceIdA
title: SetupDiGetDeviceInstanceIdA function
author: windows-sdk-content
description: The SetupDiGetDeviceInstanceId function retrieves the device instance ID that is associated with a device information element.
old-location: devinst\setupdigetdeviceinstanceid.htm
tech.root: devinst
ms.assetid: 43ad298d-2ff4-445a-aa23-1319d5f990c8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetupDiGetDeviceInstanceId, SetupDiGetDeviceInstanceId function [Device and Driver Installation], SetupDiGetDeviceInstanceIdA, SetupDiGetDeviceInstanceIdW, devinst.setupdigetdeviceinstanceid, di-rtns_f7f2bb12-37a0-489f-a1e7-0ca67600876c.xml, setupapi/SetupDiGetDeviceInstanceId
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
 - SetupDiGetDeviceInstanceId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupDiGetDeviceInstanceIdA function


## -description


The <b>SetupDiGetDeviceInstanceId</b> function retrieves the <a href="devinst.device_instance_ids">device instance ID</a> that is associated with a device information element.


## -parameters




### -param DeviceInfoSet [in]

A handle to the <a href="devinst.device_information_sets">device information set</a> that contains the device information element that represents the device for which to retrieve a device instance ID. 


### -param DeviceInfoData [in]

A pointer to an <a href="https://msdn.microsoft.com/9ad0ef4f-4a67-4f16-8bb1-2242dad0d041">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>.


### -param DeviceInstanceId [out, optional]

A pointer to the character buffer that will receive the NULL-terminated device instance ID for the specified device information element. For information about device instance IDs, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/install/device-identification-strings">Device Identification Strings</a>.


### -param DeviceInstanceIdSize [in]

The size, in characters, of the <i>DeviceInstanceId</i> buffer.


### -param RequiredSize [out, optional]

A pointer to the variable that receives the number of characters required to store the device instance ID.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by making a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/9ad0ef4f-4a67-4f16-8bb1-2242dad0d041">SP_DEVINFO_DATA</a>



<a href="https://msdn.microsoft.com/8c07db95-eb59-4e01-851d-f6a8da169625">SetupDiCreateDevRegKey</a>



<a href="https://msdn.microsoft.com/7d42167f-9af4-4aee-b641-a93ade1e3969">SetupDiCreateDeviceInfo</a>



<a href="https://msdn.microsoft.com/ffa435c8-4a73-454e-be36-cd90ba6e6d11">SetupDiOpenDevRegKey</a>



<a href="https://msdn.microsoft.com/0c4a2d09-62b2-43ce-a202-aeb59248d9fc">SetupDiOpenDeviceInfo</a>
 

 

