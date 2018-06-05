---
UID: NF:winuser.GetSystemMetricsForDpi
title: GetSystemMetricsForDpi function
author: windows-sdk-content
description: Retrieves the specified system metric or system configuration setting taking into account a provided DPI.
old-location: hidpi\getsystemmetricsfordpi.htm
old-project: hidpi
ms.assetid: E95BB417-81FA-4824-BE68-A1E3E003F8E0
ms.author: windowssdkdev
ms.date: 03/29/2018
ms.keywords: GetSystemMetricsForDpi, GetSystemMetricsForDpi function [High DPI], hidpi.getsystemmetricsfordpi, winuser/GetSystemMetricsForDpi
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: AR_STATE, *PAR_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	User32.dll
-	Ext-MS-Win-NTUser-Window-l1-1-0.dll
-	Ext-MS-Win-NTUser-Window-l1-1-1.dll
-	Ext-MS-Win-NTUser-Window-l1-1-2.dll
-	ext-ms-win-ntuser-window-l1-1-3.dll
-	Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
-	GetSystemMetricsForDpi
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetSystemMetricsForDpi function


## -description


Retrieves the specified system metric or system configuration setting taking into account a provided DPI.


## -parameters




### -param nIndex [in]

The system metric or configuration setting to be retrieved. See <a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">GetSystemMetrics</a> for the possible values.


### -param dpi [in]

The DPI to use for scaling the metric.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



This function returns the same result as <a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">GetSystemMetrics</a> but scales it according to an arbitrary DPI you provide if appropriate.



