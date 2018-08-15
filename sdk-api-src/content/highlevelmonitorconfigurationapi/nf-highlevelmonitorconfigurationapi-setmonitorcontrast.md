---
UID: NF:highlevelmonitorconfigurationapi.SetMonitorContrast
title: SetMonitorContrast function
author: windows-sdk-content
description: Sets a monitor's contrast value.
old-location: monitor\setmonitorcontrast.htm
old-project: Monitor
ms.assetid: 7957702b-0ca2-4aaa-bae7-2518d2628f64
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: SetMonitorContrast, SetMonitorContrast function [Monitor Configuration], highlevelmonitorconfigurationapi/SetMonitorContrast, monitor.setmonitorcontrast
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: highlevelmonitorconfigurationapi.h
req.include-header: 
req.redist: 
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
req.typenames: MC_SIZE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - dxva2.dll
api_name:
 - SetMonitorContrast
product: Windows
targetos: Windows
req.lib: Dxva2.lib
req.dll: Dxva2.dll
req.irql: 
req.product: GDI+ 1.1
---

# SetMonitorContrast function


## -description


Sets a monitor's contrast value.


## -parameters




### -param hMonitor [in]

Handle to a physical monitor. To get the monitor handle, call <a href="https://msdn.microsoft.com/f2ac8a6a-3be9-4155-ad13-c256b96da792">GetPhysicalMonitorsFromHMONITOR</a> or <a href="https://msdn.microsoft.com/1e0e9749-8ee4-42d5-ab7b-182222b6c429">GetPhysicalMonitorsFromIDirect3DDevice9</a>.
          


### -param dwNewContrast [in]

Contrast value. To get the monitor's minimum and maximum contrast values, call, call <a href="https://msdn.microsoft.com/996d894d-3939-418f-b7d2-c0e9d667391e">GetMonitorContrast</a>.
          


## -returns



If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.
          




## -remarks



If this function is supported, the <a href="https://msdn.microsoft.com/57cf0004-58cf-46d9-b5be-22edda2ce5a9">GetMonitorCapabilities</a> function returns the MC_CAPS_CONTRAST flag.
      

This function takes about 50 milliseconds to return.
      

The brightness setting is a continuous monitor setting. For more information, see <a href="https://msdn.microsoft.com/23e5d45d-a924-4119-b21d-b24764b53a94">Using the High-Level Monitor Configuration Functions</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/e9a00792-f471-47a4-93d7-25400e27f13f">Monitor Configuration Functions</a>
 

 

