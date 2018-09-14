---
UID: NF:winuser.SetThreadDpiAwarenessContext
title: SetThreadDpiAwarenessContext function
author: windows-sdk-content
description: Set the DPI awareness for the current thread to the provided value.
old-location: hidpi\setthreaddpiawarenesscontext.htm
tech.root: hidpi
ms.assetid: 95531BDC-3D45-4BB6-8C63-0D845C66B88F
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: SetThreadDpiAwarenessContext, SetThreadDpiAwarenessContext function [High DPI], hidpi.setthreaddpiawarenesscontext, winuser/SetThreadDpiAwarenessContext
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
 - SetThreadDpiAwarenessContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetThreadDpiAwarenessContext function


## -description


Set the DPI awareness for the current thread to the provided value.


## -parameters




### -param dpiContext [in]

The new <a href="https://msdn.microsoft.com/BFD54A9F-642B-4A3A-BBB9-F3A80779251D">DPI_AWARENESS_CONTEXT</a> for the current thread. This context includes the <a href="https://msdn.microsoft.com/0E7EB331-7D72-4853-8785-03F30263C323">DPI_AWARENESS</a> value.


## -returns



The old <a href="https://msdn.microsoft.com/BFD54A9F-642B-4A3A-BBB9-F3A80779251D">DPI_AWARENESS_CONTEXT</a> for the thread. If the <i>dpiContext</i> is invalid, the thread will not be updated and the return value will be <b>NULL</b>. You can use this value to restore the old <b>DPI_AWARENESS_CONTEXT</b> after overriding it with a predefined value.




## -remarks



Use this API to change the <a href="https://msdn.microsoft.com/BFD54A9F-642B-4A3A-BBB9-F3A80779251D">DPI_AWARENESS_CONTEXT</a> for the thread from the default value for the app.




## -see-also




<a href="https://msdn.microsoft.com/0E7EB331-7D72-4853-8785-03F30263C323">DPI_AWARENESS</a>
 

 

