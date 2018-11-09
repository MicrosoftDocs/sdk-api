---
UID: NF:winuser.GetWindowDpiAwarenessContext
title: GetWindowDpiAwarenessContext function
author: windows-sdk-content
description: Returns the DPI_AWARENESS_CONTEXT associated with a window.
old-location: hidpi\getwindowdpiawarenesscontext.htm
tech.root: hidpi
ms.assetid: BCBC6EC7-9792-43C0-BE0E-D94F00A7CAFD
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: GetWindowDpiAwarenessContext, GetWindowDpiAwarenessContext function [High DPI], hidpi.getwindowdpiawarenesscontext, winuser/GetWindowDpiAwarenessContext
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
 - GetWindowDpiAwarenessContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetWindowDpiAwarenessContext function


## -description


Returns the <a href="https://msdn.microsoft.com/BFD54A9F-642B-4A3A-BBB9-F3A80779251D">DPI_AWARENESS_CONTEXT</a> associated with a window.


## -parameters




### -param hwnd [in]

The window to query.


## -returns



The <a href="https://msdn.microsoft.com/BFD54A9F-642B-4A3A-BBB9-F3A80779251D">DPI_AWARENESS_CONTEXT</a> for the provided window. If the window is not valid, the return value is <b>NULL</b>.




## -remarks



<div class="alert"><b>Important</b>  <p class="note">The return value of <b>GetWindowDpiAwarenessContext</b> is not affected by the <a href="https://msdn.microsoft.com/0E7EB331-7D72-4853-8785-03F30263C323">DPI_AWARENESS</a> of the current thread. It only indicates the context of the window specified by the <i>hwnd</i> input parameter.

</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/0E7EB331-7D72-4853-8785-03F30263C323">DPI_AWARENESS</a>



<a href="https://msdn.microsoft.com/BE4DC6B9-BCD6-4E27-81F8-E3CF054CFBE9">GetAwarenessFromDpiAwarenessContext</a>
 

 

