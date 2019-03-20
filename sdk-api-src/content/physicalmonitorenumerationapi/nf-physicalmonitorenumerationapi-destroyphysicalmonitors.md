---
UID: NF:physicalmonitorenumerationapi.DestroyPhysicalMonitors
title: DestroyPhysicalMonitors function (physicalmonitorenumerationapi.h)
author: windows-sdk-content
description: Closes an array of physical monitor handles.
old-location: monitor\destroyphysicalmonitors.htm
tech.root: Monitor
ms.assetid: ec9bbadf-93f3-4842-9bcc-e6a76f2f1ccf
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DestroyPhysicalMonitors, DestroyPhysicalMonitors function [Monitor Configuration], monitor.destroyphysicalmonitors, physicalmonitorenumerationapi/DestroyPhysicalMonitors
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
 - DestroyPhysicalMonitors
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DestroyPhysicalMonitors function


## -description


Closes an array of physical monitor handles. Call this function to close an array of monitor handles obtained from the <a href="https://msdn.microsoft.com/f2ac8a6a-3be9-4155-ad13-c256b96da792">GetPhysicalMonitorsFromHMONITOR</a> or <a href="https://msdn.microsoft.com/1e0e9749-8ee4-42d5-ab7b-182222b6c429">GetPhysicalMonitorsFromIDirect3DDevice9</a> function.


## -parameters




### -param dwPhysicalMonitorArraySize [in]

Number of elements in the <i>pPhysicalMonitorArray</i> array.
          


### -param pPhysicalMonitorArray [in]

Pointer to an array of <a href="https://msdn.microsoft.com/en-us/library/Dd692967(v=VS.85).aspx">PHYSICAL_MONITOR</a> structures.
          


## -returns



If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/5371cbe4-80f5-4514-88e7-38107cd1a127">DestroyPhysicalMonitor Function</a>



<a href="https://msdn.microsoft.com/e9a00792-f471-47a4-93d7-25400e27f13f">Monitor Configuration Functions</a>
 

 

