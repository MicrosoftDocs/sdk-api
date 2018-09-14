---
UID: NF:highlevelmonitorconfigurationapi.GetMonitorTechnologyType
title: GetMonitorTechnologyType function
author: windows-sdk-content
description: Retrieves the type of technology used by a monitor.
old-location: monitor\getmonitortechnologytype.htm
tech.root: Monitor
ms.assetid: da3a5f64-2638-464b-973b-33cbe4cc64e7
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetMonitorTechnologyType, GetMonitorTechnologyType function [Monitor Configuration], highlevelmonitorconfigurationapi/GetMonitorTechnologyType, monitor.getmonitortechnologytype
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: highlevelmonitorconfigurationapi.h
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
req.lib: Dxva2.lib
req.dll: Dxva2.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - dxva2.dll
api_name:
 - GetMonitorTechnologyType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetMonitorTechnologyType function


## -description


Retrieves the type of technology used by a monitor.


## -parameters




### -param hMonitor [in]

Handle to a physical monitor. To get the monitor handle, call <a href="https://msdn.microsoft.com/f2ac8a6a-3be9-4155-ad13-c256b96da792">GetPhysicalMonitorsFromHMONITOR</a> or <a href="https://msdn.microsoft.com/1e0e9749-8ee4-42d5-ab7b-182222b6c429">GetPhysicalMonitorsFromIDirect3DDevice9</a>.
          


### -param pdtyDisplayTechnologyType [out]

Receives the technology type, specified as a member of the <a href="https://msdn.microsoft.com/22cb7b73-931c-4cab-a359-f957ec457148">MC_DISPLAY_TECHNOLOGY_TYPE</a> enumeration.
          


## -returns



If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.
          




## -remarks



This function does not support every display technology. If a monitor uses a display technology that is supported by this function, the <a href="https://msdn.microsoft.com/57cf0004-58cf-46d9-b5be-22edda2ce5a9">GetMonitorCapabilities</a> function returns the MC_CAPS_DISPLAY_TECHNOLOGY_TYPE flag. If that flag is absent, the <b>GetMonitorTechnologyType</b> function fails.
      

Some monitor technologies do not support certain monitor configuration functions. For example, the <a href="https://msdn.microsoft.com/8f476ba3-24d2-456a-9335-873368993d71">DegaussMonitor</a> function is supported only for cathode ray tube (CRT) monitors. To find out whether a specific function is supported, call <a href="https://msdn.microsoft.com/57cf0004-58cf-46d9-b5be-22edda2ce5a9">GetMonitorCapabilities</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/e9a00792-f471-47a4-93d7-25400e27f13f">Monitor Configuration Functions</a>
 

 

