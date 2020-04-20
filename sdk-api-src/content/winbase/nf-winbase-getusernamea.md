---
UID: NF:winbase.GetUserNameA
title: GetUserNameA function (winbase.h)
description: Retrieves the name of the user associated with the current thread.helpviewer_keywords: ["GetUserName","GetUserName function","GetUserNameA","GetUserNameW","_win32_getusername","base.getusername","winbase/GetUserName","winbase/GetUserNameA","winbase/GetUserNameW"]
old-location: base\getusername.htm
tech.root: SysInfo
ms.assetid: 87adc46a-c069-4ee5-900a-03b646306e64
ms.date: 12/05/2018
ms.keywords: GetUserName, GetUserName function, GetUserNameA, GetUserNameW, _win32_getusername, base.getusername, winbase/GetUserName, winbase/GetUserNameA, winbase/GetUserNameW
f1_keywords:
- winbase/GetUserName
dev_langs:
- c++
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetUserNameW (Unicode) and GetUserNameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Advapi32.dll
- AdvApi32Legacy.dll
- API-MS-Win-Core-SysInfo-L2-1-0.dll
api_name:
- GetUserName
- GetUserNameA
- GetUserNameW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetUserNameA function


## -description


Retrieves the name of the user associated with the current thread.

Use the 
<a href="https://docs.microsoft.com/windows/desktop/api/secext/nf-secext-getusernameexa">GetUserNameEx</a> function to retrieve the user name in a specified format. Additional information is provided by the 
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadsadsysteminfo">IADsADSystemInfo</a> interface.


## -parameters




### -param lpBuffer [out]

A pointer to the buffer to receive the user's logon name. If this buffer is not large enough to contain the entire user name, the function fails. A buffer size of (UNLEN + 1) characters will hold the maximum length user name including the terminating null character. UNLEN is defined in Lmcons.h.


### -param pcbBuffer [in, out]

On input, this variable specifies the size of the <i>lpBuffer</i> buffer, in <b>TCHARs</b>. On output, the variable receives the number of <b>TCHARs</b> copied to the buffer, including the terminating null character. 




If <i>lpBuffer</i> is too small, the function fails and <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER. This parameter receives the required buffer size, including the terminating null character.


## -returns



If the function succeeds, the return value is a nonzero value, and the variable pointed to by <i>lpnSize</i> contains the number of <b>TCHARs</b> copied to the buffer specified by <i>lpBuffer</i>, including the terminating null character.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



If the current thread is impersonating another client, the 
<b>GetUserName</b> function returns the user name of the client that the thread is impersonating.

If <b>GetUserName</b> is called from a process that is running under the  "NETWORK SERVICE" account, the string returned in <i>lpBuffer</i> may be different depending on the version of Windows.  On Windows XP, the "NETWORK SERVICE" string is returned. On Windows Vista, the “&lt;HOSTNAME&gt;$” string is returned.


#### Examples

For an example, see 
<a href="https://docs.microsoft.com/windows/desktop/SysInfo/getting-system-information">Getting System Information</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/secext/nf-secext-getusernameexa">GetUserNameEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea">LookupAccountName</a>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/system-information-functions">System Information Functions</a>
 

 

