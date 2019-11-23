---
UID: NF:physicalmonitorenumerationapi.DestroyPhysicalMonitor
title: DestroyPhysicalMonitor function (physicalmonitorenumerationapi.h)

description: Closes a handle to a physical monitor.
old-location: monitor\destroyphysicalmonitor.htm
tech.root: Monitor
ms.assetid: 5371cbe4-80f5-4514-88e7-38107cd1a127

ms.date: 12/05/2018
ms.keywords: DestroyPhysicalMonitor, DestroyPhysicalMonitor function [Monitor Configuration], monitor.destroyphysicalmonitor, physicalmonitorenumerationapi/DestroyPhysicalMonitor
ms.topic: function
f1_keywords: 
 - "physicalmonitorenumerationapi/DestroyPhysicalMonitor"
dev_langs:
 - c++
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
 - Ext-MS-Win-moderncore-Win32k-base-ntgdi-l1-1-0.dll
 - win32kfull.sys
 - win32kmin.sys
api_name:
 - DestroyPhysicalMonitor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DestroyPhysicalMonitor function


## -description


Closes a handle to a physical monitor. Call this function to close a monitor handle obtained from the <a href="https://docs.microsoft.com/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor">GetPhysicalMonitorsFromHMONITOR</a> or <a href="https://docs.microsoft.com/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9">GetPhysicalMonitorsFromIDirect3DDevice9</a> function.


## -parameters




### -param hMonitor [in]

Handle to a physical monitor.
          


## -returns



If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-destroyphysicalmonitors">DestroyPhysicalMonitors Function</a>



<a href="https://docs.microsoft.com/windows/desktop/Monitor/monitor-configuration-functions">Monitor Configuration Functions</a>
 

 

