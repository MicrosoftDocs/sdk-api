---
UID: NF:setupapi.SetupDiGetSelectedDevice
title: SetupDiGetSelectedDevice function
author: windows-sdk-content
description: The SetupDiGetSelectedDevice function retrieves the selected device information element in a device information set.
old-location: devinst\setupdigetselecteddevice.htm
old-project: devinst
ms.assetid: 317ed10b-f779-449e-8b57-329279629cc6
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: SetupDiGetSelectedDevice, SetupDiGetSelectedDevice function [Device and Driver Installation], devinst.setupdigetselecteddevice, di-rtns_c28297c0-dcc3-4bfa-9448-46ec7e9ac3a0.xml, setupapi/SetupDiGetSelectedDevice
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
 - SetupDiGetSelectedDevice
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: ADAM
---

# SetupDiGetSelectedDevice function


## -description


The <b>SetupDiGetSelectedDevice</b> function retrieves the selected device information element in a device information set. 


## -parameters




### -param DeviceInfoSet [in]

A handle to the <a href="https://msdn.microsoft.com/library/Ff541247(v=VS.85).aspx">device information set</a> for which to retrieve the selected device information element.


### -param DeviceInfoData [out]

A pointer to an <a href="https://msdn.microsoft.com/9ad0ef4f-4a67-4f16-8bb1-2242dad0d041">SP_DEVINFO_DATA</a> structure that receives information about the selected device information element for <i>DeviceInfoSet</i>. The caller must set <i>DeviceInfoData.</i><b>cbSize</b> to <b>sizeof</b>(SP_DEVINFO_DATA). If a device is currently not selected, the function fails and a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a> returns ERROR_NO_DEVICE_SELECTED.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



<b>SetupDiGetSelectedDevice</b> is usually used by an installation wizard.




## -see-also




<a href="https://msdn.microsoft.com/9ad0ef4f-4a67-4f16-8bb1-2242dad0d041">SP_DEVINFO_DATA</a>



<a href="https://msdn.microsoft.com/d3ce8a05-d26b-452f-8418-e104ae486a1a">SetupDiSetSelectedDevice</a>
 

 

