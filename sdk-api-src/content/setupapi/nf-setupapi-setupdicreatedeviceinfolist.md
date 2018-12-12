---
UID: NF:setupapi.SetupDiCreateDeviceInfoList
title: SetupDiCreateDeviceInfoList function
author: windows-sdk-content
description: The SetupDiCreateDeviceInfoList function creates an empty device information set and optionally associates the set with a device setup class and a top-level window.
old-location: devinst\setupdicreatedeviceinfolist.htm
tech.root: devinst
ms.assetid: 0596f422-39ff-41ea-8bbd-63381d418ec8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetupDiCreateDeviceInfoList, SetupDiCreateDeviceInfoList function [Device and Driver Installation], devinst.setupdicreatedeviceinfolist, di-rtns_8b7e7f05-0c72-4ae0-aee7-b88e8a59cc63.xml, setupapi/SetupDiCreateDeviceInfoList
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
 - SetupDiCreateDeviceInfoList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupDiCreateDeviceInfoList function


## -description


The <b>SetupDiCreateDeviceInfoList</b> function creates an empty <a href="https://msdn.microsoft.com/library/Ff541247(v=VS.85).aspx">device information set</a> and optionally associates the set with a <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff552344">device setup class</a> and a top-level window.


## -parameters




### -param ClassGuid [in, optional]

A pointer to the <b>GUID</b> of the device setup class to associate with the newly created device information set. If this parameter is specified, only devices of this class can be included in this device information set. If this parameter is set to <b>NULL</b>, the device information set is not associated with a specific device setup class.


### -param hwndParent [in, optional]

A handle to the top-level window to use for any user interface that is related to non-device-specific actions (such as a select-device dialog box that uses the global class driver list). This handle is optional and can be <b>NULL</b>. If a specific top-level window is not required, set <i>hwndParent</i> to <b>NULL</b>.


## -returns



The function returns a handle to an empty device information set if it is successful. Otherwise, it returns <b>INVALID_HANDLE_VALUE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The caller of this function must delete the returned device information set when it is no longer needed by calling <b>SetupDiDestroyDeviceInfoList</b>. 

To create a device information list for a remote computer use <a href="https://msdn.microsoft.com/4dae7b07-2e24-4fd8-82f2-f947296ce3c4">SetupDiCreateDeviceInfoListEx</a>.




## -see-also




<a href="https://msdn.microsoft.com/4dae7b07-2e24-4fd8-82f2-f947296ce3c4">SetupDiCreateDeviceInfoListEx</a>



<a href="https://msdn.microsoft.com/a341db0c-9ece-4677-9854-8e0dc29966c6">SetupDiDestroyDeviceInfoList</a>



<a href="https://msdn.microsoft.com/31bb0fc8-0fb8-4122-b9e8-5ff8fbbd903b">SetupDiGetClassDevs</a>



<a href="https://msdn.microsoft.com/332945dc-9edc-4fbf-a4fa-533a00352553">SetupDiGetDeviceInfoListClass</a>
 

 

