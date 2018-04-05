---
UID: NF:highlevelmonitorconfigurationapi.SetMonitorDisplayAreaSize
title: SetMonitorDisplayAreaSize function
author: windows-driver-content
description: Sets the width or height of a monitor's display area.
old-location: monitor\setmonitordisplayareasize.htm
old-project: Monitor
ms.assetid: 0c3acb13-c5db-44ce-937d-b0b001a08062
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: SetMonitorDisplayAreaSize, SetMonitorDisplayAreaSize function [Monitor Configuration], highlevelmonitorconfigurationapi/SetMonitorDisplayAreaSize, monitor.setmonitordisplayareasize
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
req.typenames: MC_SIZE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	dxva2.dll
api_name:
-	SetMonitorDisplayAreaSize
product: Windows
targetos: Windows
req.lib: Dxva2.lib
req.dll: Dxva2.dll
req.irql: 
req.product: GDI+ 1.1
---

# SetMonitorDisplayAreaSize function


## -description



        Sets the width or height of a monitor's display area.


## -parameters




### -param hMonitor [in]


            Handle to a physical monitor. To get the monitor handle, call <a href="https://msdn.microsoft.com/f2ac8a6a-3be9-4155-ad13-c256b96da792">GetPhysicalMonitorsFromHMONITOR</a> or <a href="https://msdn.microsoft.com/1e0e9749-8ee4-42d5-ab7b-182222b6c429">GetPhysicalMonitorsFromIDirect3DDevice9</a>.
          


### -param stSizeType [in]


            A member of the <a href="https://msdn.microsoft.com/6a917b7d-b91d-478a-b84e-7586d743522a">MC_SIZE_TYPE</a> enumeration, specifying whether to set the width or the height.
          


### -param dwNewDisplayAreaWidthOrHeight [in]


            Display area width or height. To get the minimum and maximum width and height, call <a href="https://msdn.microsoft.com/c27cbcf8-bb89-47c4-9f37-8b7a3d61c99f">GetMonitorDisplayAreaSize</a>.
          


## -returns




            If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.
          




## -remarks




        If this function is supported, the <a href="https://msdn.microsoft.com/57cf0004-58cf-46d9-b5be-22edda2ce5a9">GetMonitorCapabilities</a> function returns the MC_CAPS_DISPLAY_AREA_SIZE flag.
      


        This function takes about 50 milliseconds to return.
      


        The width and height settings are continuous monitor settings. For more information, see <a href="https://msdn.microsoft.com/23e5d45d-a924-4119-b21d-b24764b53a94">Using the High-Level Monitor Configuration Functions</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/e9a00792-f471-47a4-93d7-25400e27f13f">Monitor Configuration Functions</a>
 

 

