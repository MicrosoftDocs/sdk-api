---
UID: NF:winuser.GetThreadDpiHostingBehavior
title: GetThreadDpiHostingBehavior function (winuser.h)
description: Retrieves the DPI_HOSTING_BEHAVIOR from the current thread.
helpviewer_keywords: ["GetThreadDpiHostingBehavior","GetThreadDpiHostingBehavior function [High DPI]","hidpi.getthreaddpihostingbehavior","winuser/GetThreadDpiHostingBehavior"]
old-location: hidpi\getthreaddpihostingbehavior.htm
tech.root: hidpi
ms.assetid: B9500745-9B53-47FF-9F45-0BFF3A66FD46
ms.date: 12/05/2018
ms.keywords: GetThreadDpiHostingBehavior, GetThreadDpiHostingBehavior function [High DPI], hidpi.getthreaddpihostingbehavior, winuser/GetThreadDpiHostingBehavior
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetThreadDpiHostingBehavior
 - winuser/GetThreadDpiHostingBehavior
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - GetThreadDpiHostingBehavior
---

# GetThreadDpiHostingBehavior function


## -description

Retrieves the <a href="/windows/desktop/api/windef/ne-windef-dpi_hosting_behavior">DPI_HOSTING_BEHAVIOR</a> from the current thread.



## -returns

The <a href="/windows/desktop/api/windef/ne-windef-dpi_hosting_behavior">DPI_HOSTING_BEHAVIOR</a> of the current thread.

## -remarks

This API returns the hosting behavior set by an earlier call of  <a href="/windows/desktop/api/winuser/nf-winuser-setthreaddpihostingbehavior">SetThreadDpiHostingBehavior</a>, or <b>DPI_HOSTING_BEHAVIOR_DEFAULT</b> if no earlier call has been made.

## -see-also

<a href="/windows/desktop/api/windef/ne-windef-dpi_hosting_behavior">DPI_HOSTING_BEHAVIOR</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getwindowdpihostingbehavior">GetWindowDpiHostingBehavior</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setthreaddpihostingbehavior">SetThreadDpiHostingBehavior</a>
