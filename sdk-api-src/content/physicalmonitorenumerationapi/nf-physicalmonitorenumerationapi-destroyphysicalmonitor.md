---
UID: NF:physicalmonitorenumerationapi.DestroyPhysicalMonitor
title: DestroyPhysicalMonitor function
author: windows-sdk-content
description: Closes a handle to a physical monitor.
old-location: monitor\destroyphysicalmonitor.htm
old-project: Monitor
ms.assetid: 5371cbe4-80f5-4514-88e7-38107cd1a127
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: DestroyPhysicalMonitor, DestroyPhysicalMonitor function [Monitor Configuration], monitor.destroyphysicalmonitor, physicalmonitorenumerationapi/DestroyPhysicalMonitor
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
 - Ext-MS-Win-moderncore-Win32k-base-ntgdi-l1-1-0.dll
 - win32kfull.sys
 - win32kmin.sys
api_name:
 - DestroyPhysicalMonitor
product: Windows
targetos: Windows
req.lib: Dxva2.lib
req.dll: Dxva2.dll
req.irql: 
req.product: ADAM
---

# DestroyPhysicalMonitor function


## -description


Closes a handle to a physical monitor. Call this function to close a monitor handle obtained from the <a href="https://msdn.microsoft.com/f2ac8a6a-3be9-4155-ad13-c256b96da792">GetPhysicalMonitorsFromHMONITOR</a> or <a href="https://msdn.microsoft.com/1e0e9749-8ee4-42d5-ab7b-182222b6c429">GetPhysicalMonitorsFromIDirect3DDevice9</a> function.


## -parameters




### -param hMonitor [in]

Handle to a physical monitor.
          


## -returns



If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/ec9bbadf-93f3-4842-9bcc-e6a76f2f1ccf">DestroyPhysicalMonitors Function</a>



<a href="https://msdn.microsoft.com/e9a00792-f471-47a4-93d7-25400e27f13f">Monitor Configuration Functions</a>
 

 

