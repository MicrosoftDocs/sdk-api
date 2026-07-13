---
UID: NF:winnetwk.WNetGetUserW
title: WNetGetUserW function (winnetwk.h)
description: The WNetGetUser function retrieves the current default user name, or the user name used to establish a network connection. (Unicode)
helpviewer_keywords: ["WNetGetUser", "WNetGetUser function [Windows Networking (WNet)]", "WNetGetUserW", "_win32_wnetgetuser", "winnetwk/WNetGetUser", "winnetwk/WNetGetUserW", "wnet.wnetgetuser"]
old-location: wnet\wnetgetuser.htm
tech.root: WNet
ms.assetid: 8e73d2a9-c776-4661-81ab-84b7cf037cbd
ms.date: 12/05/2018
ms.keywords: WNetGetUser, WNetGetUser function [Windows Networking (WNet)], WNetGetUserA, WNetGetUserW, _win32_wnetgetuser, winnetwk/WNetGetUser, winnetwk/WNetGetUserA, winnetwk/WNetGetUserW, wnet.wnetgetuser
req.header: winnetwk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WNetGetUserW (Unicode) and WNetGetUserA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mpr.lib
req.dll: Mpr.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WNetGetUserW
 - winnetwk/WNetGetUserW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mpr.dll
api_name:
 - WNetGetUser
 - WNetGetUserA
 - WNetGetUserW
---

# WNetGetUserW function


## -description

The
				<b>WNetGetUser</b> function retrieves the current default user name, or the user name used to establish a network connection.

## -parameters

### -param lpName [in]

A pointer to a constant <b>null</b>-terminated string that specifies either the name of a local device that has been redirected to a network resource, or the remote name of a network resource to which a connection has been made without redirecting a local device.

If this parameter is <b>NULL</b> or the empty string, the system returns the name of the current user for the process.

### -param lpUserName [out]

A pointer to a buffer that receives the <b>null</b>-terminated user name.

### -param lpnLength [in, out]

A pointer to a variable that specifies the size of the <i>lpUserName</i> buffer, in characters. If the call fails because the buffer is not large enough, this variable contains the required buffer size.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a>, such as one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The device specified by the <i>lpName</i> parameter is not a redirected device or a connected network name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
More entries are available with subsequent calls.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_NETWORK</b></dt>
</dl>
</td>
<td width="60%">
The network is unavailable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_EXTENDED_ERROR</b></dt>
</dl>
</td>
<td width="60%">
A network-specific error occurred. To obtain a description of the error, call the 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetlasterrora">WNetGetLastError</a> function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_NET_OR_BAD_PATH</b></dt>
</dl>
</td>
<td width="60%">
None of the providers recognize the local name as having a connection. However, the network is not available for at least one provider to whom the connection may belong.

</td>
</tr>
</table>

## -remarks

The <b>WNetGetUser</b> function is not aware of shares on the Distributed File System (DFS). If the name specified by the <i>lpName</i> parameter is a local device  redirected to a DFS share or a remote resource that represents a DFS share, the <b>WNetGetUser</b> function fails with ERROR_NOT_CONNECTED.


#### Examples

The following code sample illustrates how to use the 
<b>WNetGetUser</b> function to retrieve the name of the user associated with a redirected local device or a remote network resource.


```cpp
#ifndef UNICODE
#define UNICODE
#endif
#pragma comment(lib, "mpr.lib")

#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <Winnetwk.h>

int wmain(int argc, wchar_t * argv[])
{
    DWORD dwRetVal;

    WCHAR UserName[MAX_PATH];

    DWORD dwNameLength = MAX_PATH;

    if (argc != 2) {
        wprintf
            (L"Usage: %s [Redirected-LocalDevice or Network-Resource-Remote-name\n",
             argv[0]);
        exit(1);
    }

    wprintf(L"Calling WNetGetUser with Network-Resource = %s\n", argv[1]);

    dwRetVal = WNetGetUser(argv[1], UserName, &dwNameLength);
    //
    // If the call succeeds, print the user information.
    //
    if (dwRetVal == NO_ERROR) {

        wprintf(L"WNetGetUser returned success\n");
        wprintf(L"\tUsername=%s   NameLength=%d\n", &UserName, dwNameLength);
        exit(0);
    }

    else {
        wprintf(L"WNetGetUser failed with error: %u\n", dwRetVal);
        exit(1);
    }
}


```






> [!NOTE]
> The winnetwk.h header defines WNetGetUser as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WNet/retrieving-the-user-name">Retrieving the User Name</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetconnectiona">WNetGetConnection</a>



<a href="/windows/desktop/WNet/windows-networking-wnet-">Windows
		  Networking (WNet) Overview</a>



<a href="/windows/desktop/WNet/windows-networking-functions">Windows
		  Networking Functions</a>
