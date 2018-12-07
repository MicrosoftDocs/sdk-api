---
UID: NF:combaseapi.CoFileTimeNow
title: CoFileTimeNow function
author: windows-sdk-content
description: Returns the current time as a FILETIME structure.
old-location: com\cofiletimenow.htm
tech.root: com
ms.assetid: 00083429-1d61-4a0b-bb73-82158869466d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CoFileTimeNow, CoFileTimeNow function [COM], _com_CoFileTimeNow, com.cofiletimenow, combaseapi/CoFileTimeNow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-OLE32-IE-l1-1-0.dll
 - ole32_wp.dll
api_name:
 - CoFileTimeNow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CoFileTimeNow function


## -description


Returns the current time as a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure.
<div class="alert"><b>Note</b>  This function is provided for compatibility with 16-bit Windows.</div><div> </div>

## -parameters




### -param lpFileTime [out]

A pointer to the <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that receives the current time.


## -returns



This function returns S_OK to indicate success.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms693800(v=VS.85).aspx">CoDosDateTimeToFileTime</a>



<a href="https://msdn.microsoft.com/en-us/library/ms680620(v=VS.85).aspx">CoFileTimeToDosDateTime</a>
 

 

