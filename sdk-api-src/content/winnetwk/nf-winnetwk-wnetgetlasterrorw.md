---
UID: NF:winnetwk.WNetGetLastErrorW
title: WNetGetLastErrorW function
author: windows-sdk-content
description: The WNetGetLastError function retrieves the most recent extended error code set by a WNet function. The network provider reported this error code; it will not generally be one of the errors included in the SDK header file WinError.h.
old-location: wnet\wnetgetlasterror.htm
tech.root: WNet
ms.assetid: 8e13c467-adcf-4e97-b51a-1f5fc919b51e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WNetGetLastError, WNetGetLastError function [Windows Networking (WNet)], WNetGetLastErrorA, WNetGetLastErrorW, _win32_wnetgetlasterror, winnetwk/WNetGetLastError, winnetwk/WNetGetLastErrorA, winnetwk/WNetGetLastErrorW, wnet.wnetgetlasterror
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winnetwk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WNetGetLastErrorW (Unicode) and WNetGetLastErrorA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mpr.lib
req.dll: Mpr.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mpr.dll
api_name:
 - WNetGetLastError
 - WNetGetLastErrorA
 - WNetGetLastErrorW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WNetGetLastErrorW function


## -description


The
				<b>WNetGetLastError</b> function retrieves the most recent extended error code set by a WNet function. The network provider reported this error code; it will not generally be one of the errors included in the SDK header file WinError.h.


## -parameters




### -param lpError [out]

Pointer to a variable that receives the error code reported by the network provider. The error code is specific to the network provider.


### -param lpErrorBuf [out]

Pointer to the buffer that receives the null-terminated string describing the error.


### -param nErrorBufSize [in]

Size of the buffer pointed to by the <i>lpErrorBuf</i> parameter, in characters. If the buffer is too small for the error string, the string is truncated but still null-terminated. A buffer of at least 256 characters is recommended.


### -param lpNameBuf [out]

Pointer to the buffer that receives the null-terminated string identifying the network provider that raised the error.


### -param nNameBufSize [in]

Size of the buffer pointed to by the <i>lpNameBuf</i> parameter, in characters. If the buffer is too small for the error string, the string is truncated but still null-terminated.


## -returns



If the function succeeds, and it obtains the last error that the network provider reported, the return value is NO_ERROR.

If the caller supplies an invalid buffer, the return value is ERROR_INVALID_ADDRESS.




## -remarks



The 
<b>WNetGetLastError</b> function retrieves errors that are specific to a network provider. You can call 
<b>WNetGetLastError</b> when a WNet function returns ERROR_EXTENDED_ERROR.

Like the 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function, 
<b>WNetGetLastError</b> returns extended error information, which is maintained on a per-thread basis. Unlike <b>GetLastError</b>, the 
<b>WNetGetLastError</b> function can return a string for reporting errors that are not described by any existing error code in WinError.h.

For more information about using an application-defined error handler that calls the 
<b>WNetGetLastError</b> function, see 
<a href="https://msdn.microsoft.com/8188304a-8ab3-4c43-a6d6-2806043cc195">Retrieving Network Errors</a>.




## -see-also




<a href="https://msdn.microsoft.com/7668ac55-7104-4ddb-88eb-920cfe4e36fd">Windows
		  Networking (WNet) Overview</a>



<a href="https://msdn.microsoft.com/95e30f8f-a326-424d-bd80-5fc9b3078dad">Windows
		  Networking Functions</a>
 

 

