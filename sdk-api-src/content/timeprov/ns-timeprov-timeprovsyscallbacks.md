---
UID: NS:timeprov.TimeProvSysCallbacks
title: TimeProvSysCallbacks
author: windows-sdk-content
description: Contains pointers to functions for use by the time provider.
old-location: base\timeprovsyscallbacks_str.htm
tech.root: sysinfo
ms.assetid: a38f8b26-9450-4033-bdd7-e73726c2d609
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: TimeProvSysCallbacks, TimeProvSysCallbacks structure, _win32_timeprovsyscallbacks_str, base.timeprovsyscallbacks_str, timeprov/TimeProvSysCallbacks
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Timeprov.h
api_name:
 - TimeProvSysCallbacks
product: Windows
targetos: Windows
req.typenames: TimeProvSysCallbacks
req.redist: 
---

# TimeProvSysCallbacks structure


## -description


Contains pointers to functions for use by the time provider.


## -struct-fields




### -field dwSize

The size of the structure, in bytes.


### -field pfnGetTimeSysInfo

A pointer to the 
<a href="https://msdn.microsoft.com/e1b527e2-ab7c-4106-b203-e74b4ce2a89b">GetTimeSysInfoFunc</a> function.


### -field pfnLogTimeProvEvent

A pointer to the 
<a href="https://msdn.microsoft.com/ddaea389-3f58-4011-bcf8-c60546d1bce1">LogTimeProvEventFunc</a> function.


### -field pfnAlertSamplesAvail

A pointer to the 
<a href="https://msdn.microsoft.com/f90da019-072e-46c9-8e05-0321a9960968">AlertSamplesAvailFunc</a> function.


### -field pfnSetProviderStatus

A pointer to the 
<a href="https://msdn.microsoft.com/e52dd1d3-081a-4fcc-85d9-a1dcef0e8011">SetProviderStatusFunc</a> function.


## -see-also




<a href="https://msdn.microsoft.com/f90da019-072e-46c9-8e05-0321a9960968">AlertSamplesAvailFunc</a>



<a href="https://msdn.microsoft.com/e1b527e2-ab7c-4106-b203-e74b4ce2a89b">GetTimeSysInfoFunc</a>



<a href="https://msdn.microsoft.com/ddaea389-3f58-4011-bcf8-c60546d1bce1">LogTimeProvEventFunc</a>



<a href="https://msdn.microsoft.com/e52dd1d3-081a-4fcc-85d9-a1dcef0e8011">SetProviderStatusFunc</a>



<a href="https://msdn.microsoft.com/cf4f8d00-4c6f-4036-a179-444ff7505ab4">TimeProvOpen</a>
 

 

