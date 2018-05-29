---
UID: NF:winuser.GetDpiFromDpiAwarenessContext
title: GetDpiFromDpiAwarenessContext function
author: windows-sdk-content
description: Retrieves the DPI from a given DPI_AWARENESS_CONTEXT handle. This enables you to determine the DPI of a thread without needed to examine a window created within that thread.
old-location: hidpi\getdpifromdpiawarenesscontext.htm
old-project: hidpi
ms.assetid: E47A7A12-AE11-4E66-AE49-463C9F4A6330
ms.author: windowssdkdev
ms.date: 03/29/2018
ms.keywords: GetDpiFromDpiAwarenessContext, GetDpiFromDpiAwarenessContext function [High DPI], hidpi.getdpifromdpiawarenesscontext, winuser/GetDpiFromDpiAwarenessContext
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
-	GetDpiFromDpiAwarenessContext
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetDpiFromDpiAwarenessContext function


## -description


Retrieves the DPI from a given <a href="https://msdn.microsoft.com/BFD54A9F-642B-4A3A-BBB9-F3A80779251D">DPI_AWARENESS_CONTEXT</a> handle. This enables you to determine the DPI of a thread without needed to examine a window created within that thread.


## -parameters




### -param value

TBD




#### - context

The <b>DPI_AWARENESS_CONTEXT</b> handle to examine.


## -returns



The DPI value associated with the <b>DPI_AWARENESS_CONTEXT</b> handle.




## -remarks




<a href="https://msdn.microsoft.com/BFD54A9F-642B-4A3A-BBB9-F3A80779251D">DPI_AWARENESS_CONTEXT</a> handles associated with values of <b>DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE</b> and <b>DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2</b> will return a value of 0 for their DPI. This is because the DPI of a per-monitor-aware window can change, and the actual DPI cannot be returned without the window's HWND.




## -see-also




<a href="https://msdn.microsoft.com/BFD54A9F-642B-4A3A-BBB9-F3A80779251D">DPI_AWARENESS_CONTEXT</a>
 

 

