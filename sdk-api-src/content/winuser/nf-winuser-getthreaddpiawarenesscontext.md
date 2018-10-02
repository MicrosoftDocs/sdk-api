---
UID: NF:winuser.GetThreadDpiAwarenessContext
title: GetThreadDpiAwarenessContext function
author: windows-sdk-content
description: Gets the DPI_AWARENESS_CONTEXT for the current thread.
old-location: hidpi\getthreaddpiawarenesscontext.htm
tech.root: hidpi
ms.assetid: DE86D551-974F-4A03-BDBE-348592CAB81F
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetThreadDpiAwarenessContext, GetThreadDpiAwarenessContext function [High DPI], hidpi.getthreaddpiawarenesscontext, winuser/GetThreadDpiAwarenessContext
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - GetThreadDpiAwarenessContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetThreadDpiAwarenessContext function


## -description


Gets the <a href="https://msdn.microsoft.com/BFD54A9F-642B-4A3A-BBB9-F3A80779251D">DPI_AWARENESS_CONTEXT</a> for the current thread.


## -parameters






## -returns



The current <a href="https://msdn.microsoft.com/BFD54A9F-642B-4A3A-BBB9-F3A80779251D">DPI_AWARENESS_CONTEXT</a> for the thread.




## -remarks



This method will return the latest <a href="https://msdn.microsoft.com/BFD54A9F-642B-4A3A-BBB9-F3A80779251D">DPI_AWARENESS_CONTEXT</a> sent to <a href="https://msdn.microsoft.com/95531BDC-3D45-4BB6-8C63-0D845C66B88F">SetThreadDpiAwarenessContext</a>. If <b>SetThreadDpiAwarenessContext</b> was never called for this thread, then the return value will equal the default <b>DPI_AWARENESS_CONTEXT</b> for the process.




## -see-also




<a href="https://msdn.microsoft.com/0E7EB331-7D72-4853-8785-03F30263C323">DPI_AWARENESS</a>



<a href="https://msdn.microsoft.com/BE4DC6B9-BCD6-4E27-81F8-E3CF054CFBE9">GetAwarenessFromDpiAwarenessContext</a>



<a href="https://msdn.microsoft.com/95531BDC-3D45-4BB6-8C63-0D845C66B88F">SetThreadDpiAwarenessContext</a>
 

 

