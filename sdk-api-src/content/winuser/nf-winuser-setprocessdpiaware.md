---
UID: NF:winuser.SetProcessDPIAware
title: SetProcessDPIAware function (winuser.h)
author: windows-sdk-content
description: SetProcessDPIAware may be altered or unavailable. Instead, use SetProcessDPIAwareness.
old-location: winmsg\setprocessdpiaware.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\setprocessdpiaware.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetProcessDPIAware, SetProcessDPIAware function [Windows and Messages], _win32_SetProcessDPIAware, _win32_setprocessdpiaware_cpp, winmsg.setprocessdpiaware, winui._win32_setprocessdpiaware, winuser/SetProcessDPIAware
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - Ext-MS-Win-RTCore-NTUser-sysparams-l1-1-0.dll
 - minuser.dll
api_name:
 - SetProcessDPIAware
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetProcessDPIAware function


## -description


<div class="alert"><b>Note</b>  It is recommended that you set the process-default DPI awareness via application manifest, not an API call. See <a href="https://msdn.microsoft.com/C9488338-D863-45DF-B5CB-7ED9B869A5E2">Setting the default DPI awareness for a process</a> for more information. Setting the process-default DPI awareness via API call can lead to unexpected application behavior.</div><div> </div>Sets the process-default DPI awareness to system-DPI awareness. This is equivalent to calling <a href="https://msdn.microsoft.com/EACD1784-BEFF-46C1-8665-CBC86A65833C">SetProcessDpiAwarenessContext</a> with a <a href="https://msdn.microsoft.com/BFD54A9F-642B-4A3A-BBB9-F3A80779251D">DPI_AWARENESS_CONTEXT</a> value of DPI_AWARENESS_CONTEXT_SYSTEM_AWARE.


## -parameters






## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the function succeeds, the return value is nonzero. Otherwise, the return value is zero.




## -remarks



For more information, see <a href="https://msdn.microsoft.com/C9488338-D863-45DF-B5CB-7ED9B869A5E2">Setting the default DPI awareness for a process</a>.




## -see-also




<a href="https://msdn.microsoft.com/C9488338-D863-45DF-B5CB-7ED9B869A5E2">Setting the default DPI awareness for a process</a>
 

 

