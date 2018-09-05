---
UID: NF:winuser.EnumWindowStationsW
title: EnumWindowStationsW function
author: windows-sdk-content
description: Enumerates all window stations in the current session. The function passes the name of each window station, in turn, to an application-defined callback function.
old-location: winstation\enumwindowstations.htm
old-project: winstation
ms.assetid: 418d4d6a-9e4d-4fe3-8e1b-398c732c6e23
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EnumWindowStations, EnumWindowStations function [Windows Stations and Desktops], EnumWindowStationsA, EnumWindowStationsW, _win32_enumwindowstations, base.enumwindowstations, winstation.enumwindowstations, winuser/EnumWindowStations, winuser/EnumWindowStationsA, winuser/EnumWindowStationsW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumWindowStationsW (Unicode) and EnumWindowStationsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - EnumWindowStations
 - EnumWindowStationsA
 - EnumWindowStationsW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# EnumWindowStationsW function


## -description


Enumerates all window stations in the current session. The function passes the name of each window station, in turn, to an application-defined callback function.


## -parameters




### -param lpEnumFunc [in]

A pointer to an application-defined 
<a href="https://msdn.microsoft.com/1b542f7e-ffc7-4c36-b82a-df44c0986abd">EnumWindowStationProc</a> callback function.


### -param lParam [in]

An application-defined value to be passed to the callback function.


## -returns



If the function succeeds, it returns the  nonzero value returned by the callback function that was pointed to by <i>lpEnumFunc</i>.

If the function is unable to perform the enumeration, the return value is zero. Call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> to get extended error information.

If the callback function fails, the return value is zero. The callback function can  call <a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> to set an error code for the caller to retrieve by calling <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>EnumWindowStations</b> function enumerates only those window stations for which the calling process has the WINSTA_ENUMERATE access right. For more information, see 
<a href="https://msdn.microsoft.com/b132da61-26b7-4457-9433-4894ca0e640a">Window Station Security and Access Rights</a>.

<b>EnumWindowStations</b> repeatedly invokes the <i>lpEnumFunc</i> callback function until the last window station is enumerated or the callback function returns FALSE.




## -see-also




<a href="https://msdn.microsoft.com/1b542f7e-ffc7-4c36-b82a-df44c0986abd">EnumWindowStationProc</a>



<a href="https://msdn.microsoft.com/6214c28f-1035-446c-8c79-5d1dd638af2a">Window Station and Desktop Functions</a>



<a href="https://msdn.microsoft.com/617661e2-3b0d-42a9-9769-2ba0957c31a8">Window Stations</a>
 

 

