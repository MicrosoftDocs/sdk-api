---
UID: NF:highlevelmonitorconfigurationapi.GetMonitorRedGreenOrBlueDrive
title: GetMonitorRedGreenOrBlueDrive function
author: windows-sdk-content
description: Retrieves a monitor's red, green, or blue drive value.
old-location: monitor\getmonitorredgreenorbluedrive.htm
old-project: Monitor
ms.assetid: 4c590d1c-be28-401a-a0e9-dacf6b86a569
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: GetMonitorRedGreenOrBlueDrive, GetMonitorRedGreenOrBlueDrive function [Monitor Configuration], highlevelmonitorconfigurationapi/GetMonitorRedGreenOrBlueDrive, monitor.getmonitorredgreenorbluedrive
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
tech.root: 
req.typenames: MC_SIZE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	dxva2.dll
api_name:
-	GetMonitorRedGreenOrBlueDrive
product: Windows
targetos: Windows
req.lib: Dxva2.lib
req.dll: Dxva2.dll
req.irql: 
req.product: GDI+ 1.1
---

# GetMonitorRedGreenOrBlueDrive function


## -description



        Retrieves a monitor's red, green, or blue drive value.


## -parameters




### -param hMonitor [in]


            Handle to a physical monitor. To get the monitor handle, call <a href="https://msdn.microsoft.com/f2ac8a6a-3be9-4155-ad13-c256b96da792">GetPhysicalMonitorsFromHMONITOR</a> or <a href="https://msdn.microsoft.com/1e0e9749-8ee4-42d5-ab7b-182222b6c429">GetPhysicalMonitorsFromIDirect3DDevice9</a>.
          


### -param dtDriveType [in]


            A member of the <a href="https://msdn.microsoft.com/bc81d258-277d-4f69-be6c-724efcdeee56">MC_DRIVE_TYPE</a> enumeration, specifying whether to retrieve the red, green, or blue drive value.
          


### -param pdwMinimumDrive [out]


            Receives the minimum red, green, or blue drive value.
          


### -param pdwCurrentDrive [out]


            Receives the current red, green, or blue drive value.
          


### -param pdwMaximumDrive [out]


            Receives the maximum red, green, or blue drive value.
          


## -returns




            If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.
          




## -remarks




        Drive settings are generally used to adjust the monitor's white point. <i>Drive</i> and <i>black level</i> are different names for the same monitor setting. If this function is supported, the <a href="https://msdn.microsoft.com/57cf0004-58cf-46d9-b5be-22edda2ce5a9">GetMonitorCapabilities</a> function returns the MC_CAPS_RED_GREEN_BLUE_DRIVE flag.
      


        This function takes about 40 milliseconds to return.
      


        The drive settings are continuous monitor settings. For more information, see <a href="https://msdn.microsoft.com/23e5d45d-a924-4119-b21d-b24764b53a94">Using the High-Level Monitor Configuration Functions</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/e9a00792-f471-47a4-93d7-25400e27f13f">Monitor Configuration Functions</a>
 

 

