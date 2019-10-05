---
UID: NF:winbase.GetCommProperties
title: GetCommProperties function (winbase.h)
author: windows-sdk-content
description: Retrieves information about the communications properties for a specified communications device.
old-location: base\getcommproperties.htm
tech.root: devio
ms.assetid: dbbf55d6-d369-4b28-bdc7-1fd9a736e658
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCommProperties, GetCommProperties function, _win32_getcommproperties, base.getcommproperties, winbase/GetCommProperties
ms.topic: function
f1_keywords:
- winbase/GetCommProperties
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
- GetCommProperties
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetCommProperties function


## -description


Retrieves information about the communications properties for a specified communications device.


## -parameters




### -param hFile [in]

A handle to the communications device. The 
<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function returns this handle.


### -param lpCommProp [out]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/ns-winbase-commprop">COMMPROP</a> structure in which the communications properties information is returned. This information can be used in subsequent calls to the 
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-setcommstate">SetCommState</a>, 
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-setcommtimeouts">SetCommTimeouts</a>, or 
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-setupcomm">SetupComm</a> function to configure the communications device.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The 
<b>GetCommProperties</b> function returns information from a device driver about the configuration settings that are supported by the driver.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/ns-winbase-commprop">COMMPROP</a>



<a href="https://docs.microsoft.com/windows/desktop/DevIO/communications-functions">Communications Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/DevIO/communications-resources">Communications Resources</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-setcommstate">SetCommState</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-setcommtimeouts">SetCommTimeouts</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-setupcomm">SetupComm</a>
 

 

