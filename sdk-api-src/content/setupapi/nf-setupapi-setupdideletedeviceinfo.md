---
UID: NF:setupapi.SetupDiDeleteDeviceInfo
title: SetupDiDeleteDeviceInfo function
author: windows-sdk-content
description: The SetupDiDeleteDeviceInfo function deletes a device information element from a device information set. This function does not delete the actual device.
old-location: devinst\setupdideletedeviceinfo.htm
old-project: devinst
ms.assetid: f510c42d-8488-4aad-a3a4-662fc8138d28
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: SetupDiDeleteDeviceInfo, SetupDiDeleteDeviceInfo function [Device and Driver Installation], devinst.setupdideletedeviceinfo, di-rtns_9bc5c091-910a-4152-acdf-eae4d86cda05.xml, setupapi/SetupDiDeleteDeviceInfo
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
api_name:
 - SetupDiDeleteDeviceInfo
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: ADAM
---

# SetupDiDeleteDeviceInfo function


## -description


The <b>SetupDiDeleteDeviceInfo</b> function deletes a device information element from a device information set. This function does not delete the actual device.


## -parameters




### -param DeviceInfoSet [in]

A handle to the <a href="https://msdn.microsoft.com/library/Ff541247(v=VS.85).aspx">device information set</a> that contains the device information element to delete.


### -param DeviceInfoData [in]

A pointer to an <a href="https://msdn.microsoft.com/9ad0ef4f-4a67-4f16-8bb1-2242dad0d041">SP_DEVINFO_DATA</a> structure that represents the device information element in <i>DeviceInfoSet </i>to delete.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



If the specified device information element is in use (for example, by a wizard page), the function fails. In this case, a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a> returns ERROR_DEVINFO_DATA_LOCKED. This happens if a handle to a wizard page is retrieved with a call to <a href="https://msdn.microsoft.com/c43ee948-10aa-4b8f-91d0-0f3baf8ccf16">SetupDiGetWizardPage</a> with this device information element specified and the DIWP_FLAG_USE_DEVINFO_DATA flag set. To delete this device information element, you must first close the wizard's HPROPSHEETPAGE handle.




## -see-also




<a href="https://msdn.microsoft.com/7d42167f-9af4-4aee-b641-a93ade1e3969">SetupDiCreateDeviceInfo</a>



<a href="https://msdn.microsoft.com/34df0557-eb86-4b00-bbd7-a4f0c1b82ff4">SetupDiEnumDeviceInfo</a>



<a href="https://msdn.microsoft.com/c43ee948-10aa-4b8f-91d0-0f3baf8ccf16">SetupDiGetWizardPage</a>



<a href="https://msdn.microsoft.com/0c4a2d09-62b2-43ce-a202-aeb59248d9fc">SetupDiOpenDeviceInfo</a>
 

 

