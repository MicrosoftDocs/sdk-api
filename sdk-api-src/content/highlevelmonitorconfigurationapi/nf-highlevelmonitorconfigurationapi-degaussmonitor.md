---
UID: NF:highlevelmonitorconfigurationapi.DegaussMonitor
title: DegaussMonitor function
author: windows-sdk-content
description: Degausses a monitor.
old-location: monitor\degaussmonitor.htm
old-project: Monitor
ms.assetid: 8f476ba3-24d2-456a-9335-873368993d71
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: DegaussMonitor, DegaussMonitor function [Monitor Configuration], highlevelmonitorconfigurationapi/DegaussMonitor, monitor.degaussmonitor
ms.prod: windows
ms.technology: windows-sdk
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
-	DegaussMonitor
product: Windows
targetos: Windows
req.lib: Dxva2.lib
req.dll: Dxva2.dll
req.irql: 
req.product: GDI+ 1.1
---

# DegaussMonitor function


## -description


Degausses a monitor. Degaussing improves a monitor's image quality and color fidelity by demagnetizing the monitor.


## -parameters




### -param hMonitor [in]


            Handle to a physical monitor. To get the monitor handle, call <a href="https://msdn.microsoft.com/f2ac8a6a-3be9-4155-ad13-c256b96da792">GetPhysicalMonitorsFromHMONITOR</a> or <a href="https://msdn.microsoft.com/1e0e9749-8ee4-42d5-ab7b-182222b6c429">GetPhysicalMonitorsFromIDirect3DDevice9</a>.
          


## -returns




            If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.
          




## -remarks




        If this function is supported, the <a href="https://msdn.microsoft.com/57cf0004-58cf-46d9-b5be-22edda2ce5a9">GetMonitorCapabilities</a> function returns the MC_CAPS_DEGAUSS flag. Degaussing is supported only by cathode ray tube (CRT) monitors.
      


        This function takes about 50 milliseconds to return.
      


        This function should not be called frequently, because calling it frequently will not noticeably improve the monitor's image quality or color fidelity.
      




## -see-also




<a href="https://msdn.microsoft.com/e9a00792-f471-47a4-93d7-25400e27f13f">Monitor Configuration Functions</a>
 

 

