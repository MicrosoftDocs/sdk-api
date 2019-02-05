---
UID: NF:winbase.FatalExit
title: FatalExit function
author: windows-sdk-content
description: Transfers execution control to the debugger. The behavior of the debugger thereafter is specific to the type of debugger used.
old-location: base\fatalexit.htm
tech.root: Debug
ms.assetid: 6015e025-872f-455a-89f9-0ff96e59ef15
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FatalExit, FatalExit function, _win32_fatalexit, base.fatalexit, winbase/FatalExit
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
 - FatalExit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FatalExit function


## -description


Transfers execution control to the debugger. The behavior of the debugger thereafter is specific to the type of debugger used.


## -parameters




### -param ExitCode [in]

The error code associated with the exit.


## -returns



This function does not return a value.




## -remarks



An application should only use 
<b>FatalExit</b> for debugging purposes. It should not call the function in a retail version of the application because doing so will terminate the application.




## -see-also




<a href="https://msdn.microsoft.com/d9e1d565-fb76-4d91-8aa7-4ff0ff31f71f">Communicating with the Debugger</a>



<a href="https://msdn.microsoft.com/95a838a2-f138-4682-b733-3f363b6c4a4b">Debugging Functions</a>



<a href="https://msdn.microsoft.com/f18d8b16-ffe1-49f1-98be-ba8d49db86ef">FatalAppExit</a>
 

 

