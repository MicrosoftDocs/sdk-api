---
UID: NF:setupapi.SetupDiDeleteDeviceInfo
title: SetupDiDeleteDeviceInfo function
author: windows-driver-content
description: The SetupDiDeleteDeviceInfo function deletes a device information element from a device information set. This function does not delete the actual device.
old-location: devinst\setupdideletedeviceinfo.htm
old-project: devinst
ms.assetid: f510c42d-8488-4aad-a3a4-662fc8138d28
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: SetupDiDeleteDeviceInfo, SetupDiDeleteDeviceInfo function [Device and Driver Installation], devinst.setupdideletedeviceinfo, di-rtns_9bc5c091-910a-4152-acdf-eae4d86cda05.xml, setupapi/SetupDiDeleteDeviceInfo
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
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Setupapi.dll
api_name:
-	SetupDiDeleteDeviceInfo
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SetupDiDeleteDeviceInfo function


## -description


The <b>SetupDiDeleteDeviceInfo</b> function deletes a device information element from a device information set. This function does not delete the actual device.


## -parameters




### -param DeviceInfoSet [in]

A handle to the <a href="devinst.device_information_sets">device information set</a> that contains the device information element to delete.


### -param DeviceInfoData [in]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552344">SP_DEVINFO_DATA</a> structure that represents the device information element in <i>DeviceInfoSet </i>to delete.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



If the specified device information element is in use (for example, by a wizard page), the function fails. In this case, a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a> returns ERROR_DEVINFO_DATA_LOCKED. This happens if a handle to a wizard page is retrieved with a call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff552019">SetupDiGetWizardPage</a> with this device information element specified and the DIWP_FLAG_USE_DEVINFO_DATA flag set. To delete this device information element, you must first close the wizard's HPROPSHEETPAGE handle.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550952">SetupDiCreateDeviceInfo</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551010">SetupDiEnumDeviceInfo</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552019">SetupDiGetWizardPage</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552071">SetupDiOpenDeviceInfo</a>
 

 

