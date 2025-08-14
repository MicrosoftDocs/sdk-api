---
UID: NF:winbase.GetCommProperties
title: GetCommProperties function (winbase.h)
description: Retrieves information about the communications properties for a specified communications device.
helpviewer_keywords: ["GetCommProperties","GetCommProperties function","_win32_getcommproperties","base.getcommproperties","winbase/GetCommProperties"]
old-location: base\getcommproperties.htm
tech.root: base
ms.assetid: dbbf55d6-d369-4b28-bdc7-1fd9a736e658
ms.date: 12/05/2018
ms.keywords: GetCommProperties, GetCommProperties function, _win32_getcommproperties, base.getcommproperties, winbase/GetCommProperties
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetCommProperties
 - winbase/GetCommProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-comm-l1-1-2.dll
 - api-ms-win-core-comm-l1-1-1.dll
 - Kernel32.dll
 - API-MS-Win-Core-comm-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - GetCommProperties
---

# GetCommProperties function


## -description

Retrieves information about the communications properties for a specified communications device.

## -parameters

### -param hFile [in]

A handle to the communications device. The 
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function returns this handle.

### -param lpCommProp [out]

A pointer to a 
<a href="/windows/desktop/api/winbase/ns-winbase-commprop">COMMPROP</a> structure in which the communications properties information is returned. This information can be used in subsequent calls to the 
<a href="/windows/desktop/api/winbase/nf-winbase-setcommstate">SetCommState</a>, 
<a href="/windows/desktop/api/winbase/nf-winbase-setcommtimeouts">SetCommTimeouts</a>, or 
<a href="/windows/desktop/api/winbase/nf-winbase-setupcomm">SetupComm</a> function to configure the communications device.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>GetCommProperties</b> function returns information from a device driver about the configuration settings that are supported by the driver.

## -see-also

<a href="/windows/desktop/api/winbase/ns-winbase-commprop">COMMPROP</a>



<a href="/windows/desktop/DevIO/communications-functions">Communications Functions</a>



<a href="/windows/desktop/DevIO/communications-resources">Communications Resources</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setcommstate">SetCommState</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setcommtimeouts">SetCommTimeouts</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setupcomm">SetupComm</a>