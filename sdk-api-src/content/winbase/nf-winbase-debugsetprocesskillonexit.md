---
UID: NF:winbase.DebugSetProcessKillOnExit
title: DebugSetProcessKillOnExit function
author: windows-sdk-content
description: Sets the action to be performed when the calling thread exits.
old-location: base\debugsetprocesskillonexit.htm
tech.root: Debug
ms.assetid: 7ef44527-bde4-41f0-a470-d3f404c77ea9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DebugSetProcessKillOnExit, DebugSetProcessKillOnExit function, _win32_debugsetprocesskillonexit, base.debugsetprocesskillonexit, winbase/DebugSetProcessKillOnExit
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - DebugSetProcessKillOnExit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DebugSetProcessKillOnExit function


## -description


Sets the action to be performed when the calling thread exits.


## -parameters




### -param KillOnExit [in]

If this parameter is <b>TRUE</b>, the thread terminates all attached processes on exit (note that this is the default). Otherwise, the thread detaches from all processes being debugged on exit.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The calling thread must have established at least one debugging connection using the <a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a> or <a href="https://msdn.microsoft.com/306a5b28-658a-4dab-a516-c638b73f4a77">DebugActiveProcess</a> function before calling this function. <b>DebugSetProcessKillOnExit</b> affects all current and future debuggees connected to the calling thread. A thread can call this function multiple times to change the action as needed.




## -see-also




<a href="https://msdn.microsoft.com/29d1a6d1-0c10-43c1-bef1-b063f07b16a4">DebugActiveProcessStop</a>



<a href="https://msdn.microsoft.com/95a838a2-f138-4682-b733-3f363b6c4a4b">Debugging Functions</a>
 

 

