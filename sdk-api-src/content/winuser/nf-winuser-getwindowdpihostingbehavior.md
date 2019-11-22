---
UID: NF:winuser.GetWindowDpiHostingBehavior
title: GetWindowDpiHostingBehavior function (winuser.h)

description: Returns the DPI_HOSTING_BEHAVIOR of the specified window.
old-location: hidpi\getwindowdpihostingbehavior.htm
tech.root: hidpi
ms.assetid: BD16F545-54A1-479A-BA4B-F54834043EB2

ms.date: 12/05/2018
ms.keywords: GetWindowDpiHostingBehavior, GetWindowDpiHostingBehavior function [High DPI], hidpi.getwindowdpihostingbehavior, winuser/GetWindowDpiHostingBehavior
ms.topic: function
f1_keywords: 
 - "winuser/GetWindowDpiHostingBehavior"
dev_langs:
 - c++
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - GetWindowDpiHostingBehavior
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetWindowDpiHostingBehavior function


## -description


Returns the <a href="https://docs.microsoft.com/windows/desktop/api/windef/ne-windef-dpi_hosting_behavior">DPI_HOSTING_BEHAVIOR</a> of the specified window.


## -parameters




### -param hwnd

The handle for the window to examine.


## -returns



The <a href="https://docs.microsoft.com/windows/desktop/api/windef/ne-windef-dpi_hosting_behavior">DPI_HOSTING_BEHAVIOR</a> of the specified window.




## -remarks



This API allows you to examine the hosting behavior of a window after it has been created. A window's hosting behavior is the hosting behavior of the thread in which the window was created, as set by a call to <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setthreaddpihostingbehavior">SetThreadDpiHostingBehavior</a>. This is a permanent value and cannot be changed after the window is created, even if the thread's hosting behavior is changed.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/windef/ne-windef-dpi_hosting_behavior">DPI_HOSTING_BEHAVIOR</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getthreaddpihostingbehavior">GetThreadDpiHostingBehavior</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setthreaddpihostingbehavior">SetThreadDpiHostingBehavior</a>
 

 

