---
UID: NF:highlevelmonitorconfigurationapi.SetMonitorDisplayAreaPosition
title: SetMonitorDisplayAreaPosition function
author: windows-sdk-content
description: Sets the horizontal or vertical position of a monitor's display area.
old-location: monitor\setmonitordisplayareaposition.htm
old-project: Monitor
ms.assetid: ad7604e5-5ede-479b-881e-0a6060182e5b
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: SetMonitorDisplayAreaPosition, SetMonitorDisplayAreaPosition function [Monitor Configuration], highlevelmonitorconfigurationapi/SetMonitorDisplayAreaPosition, monitor.setmonitordisplayareaposition
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
 - SetMonitorDisplayAreaPosition
product: Windows
targetos: Windows
req.lib: Dxva2.lib
req.dll: Dxva2.dll
req.irql: 
req.product: GDI+ 1.1
---

# SetMonitorDisplayAreaPosition function


## -description


Sets the horizontal or vertical position of a monitor's display area.

Increasing the horizontal position moves the display area toward the right side of the screen; decreasing it moves the display area toward the left. Increasing the vertical position moves the display area toward the top of the screen; decreasing it moves the display area toward the bottom.


## -parameters




### -param hMonitor [in]

Handle to a physical monitor. To get the monitor handle, call <a href="https://msdn.microsoft.com/f2ac8a6a-3be9-4155-ad13-c256b96da792">GetPhysicalMonitorsFromHMONITOR</a> or <a href="https://msdn.microsoft.com/1e0e9749-8ee4-42d5-ab7b-182222b6c429">GetPhysicalMonitorsFromIDirect3DDevice9</a>.
          


### -param ptPositionType [in]

A member of the <a href="https://msdn.microsoft.com/199e34dc-0309-4d9b-a05a-90a8bf5ab4cb">MC_POSITION_TYPE</a> enumeration, specifying whether to set the horizontal position or the vertical position.
          


### -param dwNewPosition [in]

Horizontal or vertical position. To get the minimum and maximum position, call <a href="https://msdn.microsoft.com/d6dca744-634e-420f-a025-5be9d136969f">GetMonitorDisplayAreaPosition</a>.
          


## -returns



If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.
          




## -remarks



If this function is supported, the <a href="https://msdn.microsoft.com/57cf0004-58cf-46d9-b5be-22edda2ce5a9">GetMonitorCapabilities</a> function returns the MC_CAPS_DISPLAY_AREA_POSITION flag.
      

This function takes about 50 milliseconds to return.
      

The horizontal and vertical position are continuous monitor settings. For more information, see <a href="https://msdn.microsoft.com/23e5d45d-a924-4119-b21d-b24764b53a94">Using the High-Level Monitor Configuration Functions</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/e9a00792-f471-47a4-93d7-25400e27f13f">Monitor Configuration Functions</a>
 

 

