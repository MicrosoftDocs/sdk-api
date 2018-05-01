---
UID: NF:winuser.GetThreadDpiHostingBehavior
title: GetThreadDpiHostingBehavior function
author: windows-driver-content
description: Retrieves the DPI_HOSTING_BEHAVIOR from the current thread.
old-location: hidpi\getthreaddpihostingbehavior.htm
old-project: hidpi
ms.assetid: B9500745-9B53-47FF-9F45-0BFF3A66FD46
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: GetThreadDpiHostingBehavior, GetThreadDpiHostingBehavior function [High DPI], hidpi.getthreaddpihostingbehavior, winuser/GetThreadDpiHostingBehavior
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	GetThreadDpiHostingBehavior
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetThreadDpiHostingBehavior function


## -description


Retrieves the <a href="hidpi._dpi_hosting_behavior">DPI_HOSTING_BEHAVIOR</a> from the current thread.


## -parameters






## -returns



The <a href="hidpi._dpi_hosting_behavior">DPI_HOSTING_BEHAVIOR</a> of the current thread.




## -remarks



This API returns the hosting behavior set by an earlier call of  <a href="hidpi.setthreaddpihostingbehavior">SetThreadDpiHostingBehavior</a>, or <b>DPI_HOSTING_BEHAVIOR_DEFAULT</b> if no earlier call has been made.




## -see-also




<a href="hidpi._dpi_hosting_behavior">DPI_HOSTING_BEHAVIOR</a>



<a href="hidpi.getwindowdpihostingbehavior">GetWindowDpiHostingBehavior</a>



<a href="hidpi.setthreaddpihostingbehavior">SetThreadDpiHostingBehavior</a>
 

 

