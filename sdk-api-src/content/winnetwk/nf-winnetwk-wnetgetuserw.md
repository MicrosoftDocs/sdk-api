---
UID: NF:winnetwk.WNetGetUserW
title: WNetGetUserW function
author: windows-sdk-content
description: The WNetGetUser function retrieves the current default user name, or the user name used to establish a network connection.
old-location: wnet\wnetgetuser.htm
old-project: wnet
ms.assetid: 8e73d2a9-c776-4661-81ab-84b7cf037cbd
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: WNetGetUser, WNetGetUser function [Windows Networking (WNet)], WNetGetUserA, WNetGetUserW, _win32_wnetgetuser, winnetwk/WNetGetUser, winnetwk/WNetGetUserA, winnetwk/WNetGetUserW, wnet.wnetgetuser
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winnetwk.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WINML_VARIABLE_DESC
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
product: Windows
targetos: Windows
req.lib: Mpr.lib
req.dll: Mpr.dll
req.irql: 
req.product: Windows Address Book 5.0
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
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>, such as one of the following values.

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
<a href="https://msdn.microsoft.com/8e13c467-adcf-4e97-b51a-1f5fc919b51e">WNetGetLastError</a> function.

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





## -see-also




<a href="https://msdn.microsoft.com/aed410af-d5f0-4389-882b-5b4338b5f900">Retrieving the User Name</a>



<a href="https://msdn.microsoft.com/72d84752-4e64-4c16-872b-cb892dffbf9a">WNetGetConnection</a>



<a href="https://msdn.microsoft.com/7668ac55-7104-4ddb-88eb-920cfe4e36fd">Windows
		  Networking (WNet) Overview</a>



<a href="https://msdn.microsoft.com/95e30f8f-a326-424d-bd80-5fc9b3078dad">Windows
		  Networking Functions</a>
 

 

