---
UID: NF:winbase.SetCommConfig
title: SetCommConfig function (winbase.h)

description: Sets the current configuration of a communications device.
old-location: base\setcommconfig.htm
tech.root: devio
ms.assetid: e38be757-81c6-49ae-8d90-4387893e8ec5

ms.date: 12/05/2018
ms.keywords: SetCommConfig, SetCommConfig function, _win32_setcommconfig, base.setcommconfig, winbase/SetCommConfig
ms.topic: function
f1_keywords:
- winbase/SetCommConfig
dev_langs:
 - c++
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
- API-MS-Win-Core-comm-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
- MinKernelBase.dll
api_name:
- SetCommConfig
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetCommConfig function


## -description


Sets the current configuration of a communications device.


## -parameters




### -param hCommDev [in]

A handle to the open communications device. The 
<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function returns this handle.


### -param lpCC [in]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/ns-winbase-commconfig">COMMCONFIG</a> structure.


### -param dwSize [in]

The size of the structure pointed to by <i>lpCC</i>, in bytes.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/ns-winbase-commconfig">COMMCONFIG</a>



<a href="https://docs.microsoft.com/windows/desktop/DevIO/communications-functions">Communications Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/DevIO/communications-resources">Communications Resources</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-getcommconfig">GetCommConfig</a>
 

 

