---
UID: NF:fltuser.FilterUnload
title: FilterUnload function
author: windows-sdk-content
description: An application that has loaded a supporting minifilter by calling FilterLoad can unload the minifilter by calling the FilterUnload function.
old-location: ifsk\filterunload.htm
old-project: ifsk
ms.assetid: 74de2531-1666-420e-b500-131622f1b76f
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: FilterUnload, FilterUnload function [Installable File System Drivers], FltWin32ApiRef_d6c75950-e58b-4f4c-8707-85566c03d219.xml, fltuser/FilterUnload, ifsk.filterunload
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: fltuser.h
req.include-header: Fltuser.h
req.target-type: Universal
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
tech.root: 
req.typenames: FILTERED_DATA_SOURCES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	FltLib.dll
api_name:
-	FilterUnload
product: Windows
targetos: Windows
req.lib: FltLib.lib
req.dll: FltLib.dll
req.irql: 
req.product: Internet Explorer 5
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
 

 

