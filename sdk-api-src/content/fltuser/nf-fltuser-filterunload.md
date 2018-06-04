---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# FilterUnload function


## -description


An application that has loaded a supporting minifilter by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff541504">FilterLoad</a> can unload the minifilter by calling the <b>FilterUnload</b> function. 


## -parameters




### -param lpFilterName [in]

Pointer to a null-terminated wide-character string containing the same minifilter name that was passed to <a href="https://msdn.microsoft.com/library/windows/hardware/ff541504">FilterLoad</a>. This parameter is required and cannot be <b>NULL</b> or an empty string. 


## -returns



<b>FilterUnload</b> returns S_OK if successful. Otherwise, it returns an error value. 




## -remarks



<b>FilterUnload</b> is the Win32 equivalent of <a href="https://msdn.microsoft.com/library/windows/hardware/ff544602">FltUnloadFilter</a>. 

<b>FilterUnload</b> searches for a registered minifilter whose service name matches the given <i>lpFilterName</i> and calls that minifilter's <i>FilterUnloadCallback</i> (<a href="https://msdn.microsoft.com/library/windows/hardware/ff551085">PFLT_FILTER_UNLOAD_CALLBACK</a>) routine. 

If the minifilter did not register a <i>FilterUnloadCallback</i> routine, the call to <b>FilterUnload</b> fails. 

Callers of <b>FilterUnload</b> must have <b>SeLoadDriverPrivilege</b> (the LUID of SE_LOAD_DRIVER_PRIVILEGE) to load or unload a minifilter driver. This privilege is named by the SE_LOAD_DRIVER_NAME name constant. (Privileges are described in the Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0 documentation.) 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff541504">FilterLoad</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544602">FltUnloadFilter</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551085">PFLT_FILTER_UNLOAD_CALLBACK</a>
 

 

