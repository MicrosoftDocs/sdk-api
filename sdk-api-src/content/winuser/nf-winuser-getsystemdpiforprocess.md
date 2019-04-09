---
UID: NF:winuser.GetSystemDpiForProcess
title: GetSystemDpiForProcess function (winuser.h)
author: windows-sdk-content
description: Retrieves the system DPI associated with a given process. This is useful for avoiding compatibility issues that arise from sharing DPI-sensitive information between multiple system-aware processes with different system DPI values.
old-location: hidpi\getsystemdpiforprocess.htm
tech.root: hidpi
ms.assetid: 94236ECF-E69A-4D77-AABA-D43FE8DF8203
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetSystemDpiForProcess, GetSystemDpiForProcess function [High DPI], hidpi.getsystemdpiforprocess, winuser/GetSystemDpiForProcess
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
 - GetSystemDpiForProcess
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetSystemDpiForProcess function


## -description


Retrieves the system DPI associated with a given process. This is useful for avoiding compatibility issues that arise from sharing DPI-sensitive information between multiple system-aware processes with different system DPI values.


## -parameters




### -param hProcess

The handle for the process to examine. If this value is null, this API behaves identically to <a href="https://msdn.microsoft.com/B744EC4A-DB78-4654-B50F-C27CB7702899">GetDpiForSystem</a>.


## -returns



The process's system DPI value.




## -remarks



The return value will be dependent based upon the process passed as a parameter. If the specified process has a <a href="https://msdn.microsoft.com/0E7EB331-7D72-4853-8785-03F30263C323">DPI_AWARENESS</a> value of <b>DPI_AWARENESS_UNAWARE</b>, the return value will be 96. That is because the current context always assumes a DPI of 96. For any other <b>DPI_AWARENESS</b> value, the return value will be the actual system DPI of the given process.






## -see-also




<a href="https://msdn.microsoft.com/0E7EB331-7D72-4853-8785-03F30263C323">DPI_AWARENESS</a>



<a href="https://msdn.microsoft.com/B744EC4A-DB78-4654-B50F-C27CB7702899">GetDpiForSystem</a>
 

 

