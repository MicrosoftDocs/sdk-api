---
UID: NF:setupapi.SetupDiDestroyDeviceInfoList
title: SetupDiDestroyDeviceInfoList function (setupapi.h)
author: windows-sdk-content
description: The SetupDiDestroyDeviceInfoList function deletes a device information set and frees all associated memory.
old-location: devinst\setupdidestroydeviceinfolist.htm
tech.root: devinst
ms.assetid: a341db0c-9ece-4677-9854-8e0dc29966c6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetupDiDestroyDeviceInfoList, SetupDiDestroyDeviceInfoList function [Device and Driver Installation], devinst.setupdidestroydeviceinfolist, di-rtns_f8a4a633-46fd-4d3f-81dc-68920ccebfd9.xml, setupapi/SetupDiDestroyDeviceInfoList
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
 - Ext-MS-Win-SetupAPI-ClassInstallers-l1-1-0.dll
 - Ext-MS-Win-SetupAPI-ClassInstallers-l1-1-1.dll
 - Ext-MS-Win-SetupAPI-ClassInstallers-L1-1-2.dll
api_name:
 - SetupDiDestroyDeviceInfoList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupDiDestroyDeviceInfoList function


## -description


The <b>SetupDiDestroyDeviceInfoList</b> function deletes a device information set and frees all associated memory.


## -parameters




### -param DeviceInfoSet [in]

A handle to the <a href="https://msdn.microsoft.com/library/Ff541247(v=VS.85).aspx">device information set</a> to delete.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/0596f422-39ff-41ea-8bbd-63381d418ec8">SetupDiCreateDeviceInfoList</a>



<a href="https://msdn.microsoft.com/31bb0fc8-0fb8-4122-b9e8-5ff8fbbd903b">SetupDiGetClassDevs</a>
 

 

