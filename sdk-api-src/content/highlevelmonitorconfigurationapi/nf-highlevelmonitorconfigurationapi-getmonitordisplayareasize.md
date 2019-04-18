---
UID: NF:highlevelmonitorconfigurationapi.GetMonitorDisplayAreaSize
title: GetMonitorDisplayAreaSize function (highlevelmonitorconfigurationapi.h)
author: windows-sdk-content
description: Retrieves a monitor's minimum, maximum, and current width or height.
old-location: monitor\getmonitordisplayareasize.htm
tech.root: Monitor
ms.assetid: c27cbcf8-bb89-47c4-9f37-8b7a3d61c99f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetMonitorDisplayAreaSize, GetMonitorDisplayAreaSize function [Monitor Configuration], highlevelmonitorconfigurationapi/GetMonitorDisplayAreaSize, monitor.getmonitordisplayareasize
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
 - GetMonitorDisplayAreaSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetMonitorDisplayAreaSize function


## -description


Retrieves a monitor's minimum, maximum, and current width or height.


## -parameters




### -param hMonitor [in]

Handle to a physical monitor. To get the monitor handle, call <a href="https://msdn.microsoft.com/f2ac8a6a-3be9-4155-ad13-c256b96da792">GetPhysicalMonitorsFromHMONITOR</a> or <a href="https://msdn.microsoft.com/1e0e9749-8ee4-42d5-ab7b-182222b6c429">GetPhysicalMonitorsFromIDirect3DDevice9</a>.
          


### -param stSizeType [in]

A member of the <a href="https://msdn.microsoft.com/en-us/library/Dd692959(v=VS.85).aspx">MC_SIZE_TYPE</a> enumeration, specifying whether to retrieve the width or the height.
          


### -param pdwMinimumWidthOrHeight [out]

Receives the minimum width or height.
          


### -param pdwCurrentWidthOrHeight [out]

Receives the current width or height.
          


### -param pdwMaximumWidthOrHeight [out]

Receives the maximum width or height.
          


## -returns



If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.
          




## -remarks



If this function is supported, the <a href="https://msdn.microsoft.com/57cf0004-58cf-46d9-b5be-22edda2ce5a9">GetMonitorCapabilities</a> function returns the MC_CAPS_DISPLAY_AREA_SIZE flag.
      

This function takes about 40 milliseconds to return.
      

The width and height settings are continuous monitor settings. For more information, see <a href="https://msdn.microsoft.com/23e5d45d-a924-4119-b21d-b24764b53a94">Using the High-Level Monitor Configuration Functions</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/e9a00792-f471-47a4-93d7-25400e27f13f">Monitor Configuration Functions</a>
 

 

