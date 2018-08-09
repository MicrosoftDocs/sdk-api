---
UID: NF:physicalmonitorenumerationapi.GetNumberOfPhysicalMonitorsFromHMONITOR
title: GetNumberOfPhysicalMonitorsFromHMONITOR function
author: windows-sdk-content
description: Retrieves the number of physical monitors associated with an HMONITOR monitor handle.
old-location: monitor\getnumberofphysicalmonitorsfromhmonitor.htm
old-project: Monitor
ms.assetid: c4cc3012-10ae-4435-8d81-e0a9eb62b55c
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetNumberOfPhysicalMonitorsFromHMONITOR, GetNumberOfPhysicalMonitorsFromHMONITOR function [Monitor Configuration], monitor.getnumberofphysicalmonitorsfromhmonitor, physicalmonitorenumerationapi/GetNumberOfPhysicalMonitorsFromHMONITOR
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: physicalmonitorenumerationapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: USER_INPUT_STRING_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - dxva2.dll
api_name:
 - GetNumberOfPhysicalMonitorsFromHMONITOR
product: Windows
targetos: Windows
req.lib: Dxva2.lib
req.dll: Dxva2.dll
req.irql: 
req.product: ADAM
---

# GetNumberOfPhysicalMonitorsFromHMONITOR function


## -description


Retrieves the number of physical monitors associated with an <b>HMONITOR</b> monitor handle. Call this function before calling <a href="https://msdn.microsoft.com/f2ac8a6a-3be9-4155-ad13-c256b96da792">GetPhysicalMonitorsFromHMONITOR</a>.
      


## -parameters




### -param hMonitor [in]

A monitor handle. Monitor handles are returned by several Multiple Display Monitor functions, including <a href="https://msdn.microsoft.com/a7668c28-77c9-4373-ae1a-eab3cb98f866">EnumDisplayMonitors</a> and <a href="https://msdn.microsoft.com/fe6505c9-b481-4fec-ae9d-995943234a3a">MonitorFromWindow</a>, which are part of the graphics device interface (GDI).
          


### -param pdwNumberOfPhysicalMonitors [out]

Receives the number of physical monitors associated with the monitor handle.
          


## -returns



If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.
          




## -see-also




<a href="https://msdn.microsoft.com/f2ac8a6a-3be9-4155-ad13-c256b96da792">GetPhysicalMonitorsFromHMONITOR</a>



<a href="https://msdn.microsoft.com/e9a00792-f471-47a4-93d7-25400e27f13f">Monitor Configuration Functions</a>
 

 

