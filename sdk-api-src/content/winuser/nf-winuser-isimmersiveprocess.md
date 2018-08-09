---
UID: NF:winuser.IsImmersiveProcess
title: IsImmersiveProcess function
author: windows-sdk-content
description: Determines whether the process belongs to a Windows Store app.
old-location: base\isimmersiveprocess.htm
old-project: procthread
ms.assetid: E95FD9C0-8E4A-44FA-BBA6-0A7F53A0E584
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IsImmersiveProcess, IsImmersiveProcess function, base.isimmersiveprocess, winuser/IsImmersiveProcess
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-uicontext-Ext-l1-1-0.dll
 - modernapiexthost.dll
 - api-ms-win-ntuser-uicontext-l1-1-0.dll
api_name:
 - IsImmersiveProcess
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IsImmersiveProcess function


## -description


Determines whether the process belongs to a Windows Store app.


## -parameters




### -param hProcess [in]

Target process handle.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.



