---
UID: NF:setupapi.SetupDiGetDeviceInfoListClass
title: SetupDiGetDeviceInfoListClass function
author: windows-sdk-content
description: The SetupDiGetDeviceInfoListClass function retrieves the GUID for the device setup class associated with a device information set if the set has an associated class.
old-location: devinst\setupdigetdeviceinfolistclass.htm
old-project: devinst
ms.assetid: 332945dc-9edc-4fbf-a4fa-533a00352553
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SetupDiGetDeviceInfoListClass, SetupDiGetDeviceInfoListClass function [Device and Driver Installation], devinst.setupdigetdeviceinfolistclass, di-rtns_219b6225-e6f3-40b4-8127-709c425a0cad.xml, setupapi/SetupDiGetDeviceInfoListClass
ms.prod: windows
ms.technology: windows-sdk
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
 - SetupDiGetDeviceInfoListClass
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: ADAM
---

# SetupDiGetDeviceInfoListClass function


## -description


The <b>SetupDiGetDeviceInfoListClass</b> function retrieves the GUID for the <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff552344">device setup class</a> associated with a device information set if the set has an associated class.


## -parameters




### -param DeviceInfoSet [in]

A handle to the <a href="devinst.device_information_sets">device information set</a> to query.


### -param ClassGuid [out]

A pointer to variable of type GUID that receives the GUID for the associated class.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



If the specified device information set does not have an associated class because a class GUID was not specified when the set was created with <a href="https://msdn.microsoft.com/library/windows/hardware/ff550956">SetupDiCreateDeviceInfoList</a>, the function fails. In this case, a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a> returns ERROR_NO_ASSOCIATED_CLASS.

If a device information set is for a remote computer, use <a href="https://msdn.microsoft.com/library/windows/hardware/ff551103">SetupDiGetDeviceInfoListDetail</a> to get the associated remote computer handle and computer name.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550956">SetupDiCreateDeviceInfoList</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551069">SetupDiGetClassDevs</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551103">SetupDiGetDeviceInfoListDetail</a>
 

 

