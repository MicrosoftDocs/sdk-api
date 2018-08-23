---
UID: NF:setupapi.SetupDiEnumDeviceInfo
title: SetupDiEnumDeviceInfo function
author: windows-sdk-content
description: The SetupDiEnumDeviceInfo function returns a SP_DEVINFO_DATA structure that specifies a device information element in a device information set.
old-location: devinst\setupdienumdeviceinfo.htm
old-project: devinst
ms.assetid: 34df0557-eb86-4b00-bbd7-a4f0c1b82ff4
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: SetupDiEnumDeviceInfo, SetupDiEnumDeviceInfo function [Device and Driver Installation], devinst.setupdienumdeviceinfo, di-rtns_db6730f9-381a-4da6-91b1-046fec51f270.xml, setupapi/SetupDiEnumDeviceInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: setupapi.h
req.include-header: Setupapi.h
req.redist: 
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
tech.root: 
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
 - Ext-MS-Win-SetupAPI-ClassInstallers-l1-1-0.dll
 - Ext-MS-Win-SetupAPI-ClassInstallers-l1-1-1.dll
 - Ext-MS-Win-SetupAPI-ClassInstallers-L1-1-2.dll
api_name:
 - SetupDiEnumDeviceInfo
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: ADAM
---

# SetupDiEnumDeviceInfo function


## -description


The <b>SetupDiEnumDeviceInfo</b> function returns a <a href="https://msdn.microsoft.com/9ad0ef4f-4a67-4f16-8bb1-2242dad0d041">SP_DEVINFO_DATA</a> structure that specifies a device information element in a device information set. 


## -parameters




### -param DeviceInfoSet [in]

A handle to the <a href="https://msdn.microsoft.com/library/Ff541247(v=VS.85).aspx">device information set</a> for which to return an <a href="https://msdn.microsoft.com/9ad0ef4f-4a67-4f16-8bb1-2242dad0d041">SP_DEVINFO_DATA</a> structure that represents a device information element.


### -param MemberIndex [in]

A zero-based index of the device information element to retrieve.


### -param DeviceInfoData [out]

A pointer to an <a href="https://msdn.microsoft.com/9ad0ef4f-4a67-4f16-8bb1-2242dad0d041">SP_DEVINFO_DATA</a> structure to receive information about an enumerated device information element. The caller must set <i>DeviceInfoData</i>.<b>cbSize</b> to <code>sizeof(SP_DEVINFO_DATA)</code>.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



Repeated calls to this function return a device information element for a different device. This function can be called repeatedly to get information about all devices in the device information set.

To enumerate device information elements, an installer should initially call <b>SetupDiEnumDeviceInfo</b> with the <i>MemberIndex</i> parameter set to 0. The installer should then increment <i>MemberIndex</i> and call <b>SetupDiEnumDeviceInfo</b> until there are no more values (the function fails and a call to <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>ERROR_NO_MORE_ITEMS</b>).

Call <a href="https://msdn.microsoft.com/5095404d-2447-407e-99e2-dd3ef3c3b905">SetupDiEnumDeviceInterfaces</a> to get a context structure for a device <i>interface</i> element (versus a device <i>information</i> element).




## -see-also




<a href="https://msdn.microsoft.com/9ad0ef4f-4a67-4f16-8bb1-2242dad0d041">SP_DEVINFO_DATA</a>



<a href="https://msdn.microsoft.com/7d42167f-9af4-4aee-b641-a93ade1e3969">SetupDiCreateDeviceInfo</a>



<a href="https://msdn.microsoft.com/f510c42d-8488-4aad-a3a4-662fc8138d28">SetupDiDeleteDeviceInfo</a>



<a href="https://msdn.microsoft.com/5095404d-2447-407e-99e2-dd3ef3c3b905">SetupDiEnumDeviceInterfaces</a>



<a href="https://msdn.microsoft.com/0c4a2d09-62b2-43ce-a202-aeb59248d9fc">SetupDiOpenDeviceInfo</a>
 

 

