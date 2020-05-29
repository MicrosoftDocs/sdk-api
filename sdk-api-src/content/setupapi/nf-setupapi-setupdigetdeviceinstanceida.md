---
UID: NF:setupapi.SetupDiGetDeviceInstanceIdA
title: SetupDiGetDeviceInstanceIdA function (setupapi.h)
description: The SetupDiGetDeviceInstanceId function retrieves the device instance ID that is associated with a device information element.
helpviewer_keywords: ["SetupDiGetDeviceInstanceId","SetupDiGetDeviceInstanceId function [Device and Driver Installation]","SetupDiGetDeviceInstanceIdA","SetupDiGetDeviceInstanceIdW","devinst.setupdigetdeviceinstanceid","di-rtns_f7f2bb12-37a0-489f-a1e7-0ca67600876c.xml","setupapi/SetupDiGetDeviceInstanceId"]
old-location: devinst\setupdigetdeviceinstanceid.htm
tech.root: devinst
ms.assetid: 43ad298d-2ff4-445a-aa23-1319d5f990c8
ms.date: 12/05/2018
ms.keywords: SetupDiGetDeviceInstanceId, SetupDiGetDeviceInstanceId function [Device and Driver Installation], SetupDiGetDeviceInstanceIdA, SetupDiGetDeviceInstanceIdW, devinst.setupdigetdeviceinstanceid, di-rtns_f7f2bb12-37a0-489f-a1e7-0ca67600876c.xml, setupapi/SetupDiGetDeviceInstanceId
f1_keywords:
- setupapi/SetupDiGetDeviceInstanceId
dev_langs:
- c++
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
- SetupDiGetDeviceInstanceId - SetupDiGetDeviceInstanceIdA
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetupDiGetDeviceInstanceIdA function


## -description


The <b>SetupDiGetDeviceInstanceId</b> function retrieves the <a href="https://docs.microsoft.com/windows-hardware/drivers/install/device-instance-ids">device instance ID</a> that is associated with a device information element.


## -parameters




### -param DeviceInfoSet [in]

A handle to the <a href="https://docs.microsoft.com/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains the device information element that represents the device for which to retrieve a device instance ID. 


### -param DeviceInfoData [in]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>.


### -param DeviceInstanceId [out, optional]

A pointer to the character buffer that will receive the NULL-terminated device instance ID for the specified device information element. For information about device instance IDs, see <a href="https://docs.microsoft.com/windows-hardware/drivers/install/device-identification-strings">Device Identification Strings</a>.


### -param DeviceInstanceIdSize [in]

The size, in characters, of the <i>DeviceInstanceId</i> buffer.


### -param RequiredSize [out, optional]

A pointer to the variable that receives the number of characters required to store the device instance ID.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by making a call to <a href="https://msdn.microsoft.com/library/ms679360(VS.85).aspx">GetLastError</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupdicreatedevregkeya">SetupDiCreateDevRegKey</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupdicreatedeviceinfoa">SetupDiCreateDeviceInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupdiopendevregkey">SetupDiOpenDevRegKey</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupdiopendeviceinfoa">SetupDiOpenDeviceInfo</a>
 

 

## -remarks

> [!NOTE]
> The setupapi.h header defines SetupDiGetDeviceInstanceId as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

