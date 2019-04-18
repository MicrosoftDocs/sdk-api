---
UID: NF:winuser.GetThreadDpiHostingBehavior
title: GetThreadDpiHostingBehavior function (winuser.h)
author: windows-sdk-content
description: Retrieves the DPI_HOSTING_BEHAVIOR from the current thread.
old-location: hidpi\getthreaddpihostingbehavior.htm
tech.root: hidpi
ms.assetid: B9500745-9B53-47FF-9F45-0BFF3A66FD46
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetThreadDpiHostingBehavior, GetThreadDpiHostingBehavior function [High DPI], hidpi.getthreaddpihostingbehavior, winuser/GetThreadDpiHostingBehavior
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
 - GetThreadDpiHostingBehavior
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetThreadDpiHostingBehavior function


## -description


Retrieves the <a href="https://msdn.microsoft.com/4BFBF485-1AD2-4460-A4EE-CB76EF62B8C4">DPI_HOSTING_BEHAVIOR</a> from the current thread.


## -parameters






## -returns



The <a href="https://msdn.microsoft.com/4BFBF485-1AD2-4460-A4EE-CB76EF62B8C4">DPI_HOSTING_BEHAVIOR</a> of the current thread.




## -remarks



This API returns the hosting behavior set by an earlier call of  <a href="https://msdn.microsoft.com/CF31D96A-EC84-4911-81A2-82EC90D417B9">SetThreadDpiHostingBehavior</a>, or <b>DPI_HOSTING_BEHAVIOR_DEFAULT</b> if no earlier call has been made.




## -see-also




<a href="https://msdn.microsoft.com/4BFBF485-1AD2-4460-A4EE-CB76EF62B8C4">DPI_HOSTING_BEHAVIOR</a>



<a href="https://msdn.microsoft.com/BD16F545-54A1-479A-BA4B-F54834043EB2">GetWindowDpiHostingBehavior</a>



<a href="https://msdn.microsoft.com/CF31D96A-EC84-4911-81A2-82EC90D417B9">SetThreadDpiHostingBehavior</a>
 

 

