---
UID: NF:winuser.GetWindowDpiHostingBehavior
title: GetWindowDpiHostingBehavior function
author: windows-sdk-content
description: Returns the DPI_HOSTING_BEHAVIOR of the specified window.
old-location: hidpi\getwindowdpihostingbehavior.htm
old-project: hidpi
ms.assetid: BD16F545-54A1-479A-BA4B-F54834043EB2
ms.author: windowssdkdev
ms.date: 03/29/2018
ms.keywords: GetWindowDpiHostingBehavior, GetWindowDpiHostingBehavior function [High DPI], hidpi.getwindowdpihostingbehavior, winuser/GetWindowDpiHostingBehavior
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AR_STATE, *PAR_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	User32.dll
api_name:
-	GetWindowDpiHostingBehavior
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetWindowDpiHostingBehavior function


## -description


Returns the <a href="hidpi._dpi_hosting_behavior">DPI_HOSTING_BEHAVIOR</a> of the specified window.


## -parameters




### -param hwnd

The handle for the window to examine.


## -returns



The <a href="hidpi._dpi_hosting_behavior">DPI_HOSTING_BEHAVIOR</a> of the specified window.




## -remarks



This API allows you to examine the hosting behavior of a window after it has been created. A window's hosting behavior is the hosting behavior of the thread in which the window was created, as set by a call to <a href="hidpi.setthreaddpihostingbehavior">SetThreadDpiHostingBehavior</a>. This is a permanent value and cannot be changed after the window is created, even if the thread's hosting behavior is changed.




## -see-also




<a href="hidpi._dpi_hosting_behavior">DPI_HOSTING_BEHAVIOR</a>



<a href="hidpi.getthreaddpihostingbehavior">GetThreadDpiHostingBehavior</a>



<a href="hidpi.setthreaddpihostingbehavior">SetThreadDpiHostingBehavior</a>
 

 

