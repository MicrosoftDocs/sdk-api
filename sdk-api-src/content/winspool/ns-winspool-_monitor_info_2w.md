---
UID: NS:winspool._MONITOR_INFO_2W
title: "_MONITOR_INFO_2W"
author: windows-driver-content
description: The MONITOR_INFO_2 structure identifies a monitor.
old-location: gdi\monitor_info_2.htm
old-project: printdocs
ms.assetid: 4dd1ca15-6983-403e-8159-1a6d35a88162
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPMONITOR_INFO_2W, *PMONITOR_INFO_2W, MONITOR_INFO_2, MONITOR_INFO_2 structure [Windows GDI], MONITOR_INFO_2W, PMONITOR_INFO_2, PMONITOR_INFO_2 structure pointer [Windows GDI], _MONITOR_INFO_2A, _MONITOR_INFO_2W, _win32_MONITOR_INFO_2_str, gdi.monitor_info_2, winspool/MONITOR_INFO_2, winspool/PMONITOR_INFO_2, winspool/_MONITOR_INFO_2A, winspool/_MONITOR_INFO_2W"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winspool.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: "_MONITOR_INFO_2W (Unicode) and _MONITOR_INFO_2A (ANSI)"
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MONITOR_INFO_2W, *PMONITOR_INFO_2W, *LPMONITOR_INFO_2W
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	MONITOR_INFO_2
-	_MONITOR_INFO_2A
-	_MONITOR_INFO_2W
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _MONITOR_INFO_2W structure


## -description



The <b>MONITOR_INFO_2</b> structure identifies a monitor.




## -struct-fields




### -field pName

A pointer to a null-terminated string that is the name of the monitor.


### -field pEnvironment

A pointer to a null-terminated string that specifies the environment for which the monitor was written (for example, Windows NT x86, Windows IA64, Windows x64).


### -field pDLLName

A pointer to a null-terminated string that is the name of the monitor DLL.


## -see-also




<a href="https://msdn.microsoft.com/6a556422-5360-42d2-b177-dba0498c06d8">AddMonitor</a>



<a href="https://msdn.microsoft.com/4d4fbed2-193f-426c-8463-eeb6b1eaf316">EnumMonitors</a>



<a href="https://msdn.microsoft.com/7a4660bd-5df8-49dd-92f6-9574f451f10d">MONITOR_INFO_1</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

