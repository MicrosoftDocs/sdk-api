---
UID: NF:timeprov.TimeProvClose
title: TimeProvClose function
author: windows-sdk-content
description: A callback function that is called by the time provider manager to shut down the time provider.
old-location: base\timeprovclose.htm
old-project: SysInfo
ms.assetid: ca8f5c8b-8c46-46eb-8d15-4c0c8a8437dd
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: TimeProvClose, TimeProvClose callback, TimeProvClose callback function, _win32_timeprovclose, base.timeprovclose, timeprov/TimeProvClose
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: timeprov.h
req.include-header: 
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
tech.root: 
req.typenames: TIMECAPS, *PTIMECAPS, *NPTIMECAPS, *LPTIMECAPS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Timeprov.h
api_name:
 - TimeProvClose
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# TimeProvClose function


## -description


A  callback function that is called by the time provider manager to shut down the time provider.


## -parameters




### -param hTimeProv [in]

A handle to the time provider. The 
<a href="https://msdn.microsoft.com/cf4f8d00-4c6f-4036-a179-444ff7505ab4">TimeProvOpen</a> function receives this handle.


## -returns



If the function succeeds, the return value is S_OK. Otherwise, the return value is one of the error codes defined in WinError.h.




## -remarks



The provider should clean up its resources and terminate its operation. When the function returns, the time provider manager can unload the DLL. Therefore, the handle to the time provider is no longer valid and should not be used again.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/6be08c49-be68-4b75-b740-fc1d5a2ff592">Sample Time Provider</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/cf4f8d00-4c6f-4036-a179-444ff7505ab4">TimeProvOpen</a>
 

 

