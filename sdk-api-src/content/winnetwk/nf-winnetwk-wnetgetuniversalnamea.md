---
UID: NF:winnetwk.WNetGetUniversalNameA
title: WNetGetUniversalNameA function (winnetwk.h)
description: The WNetGetUniversalName function takes a drive-based path for a network resource and returns an information structure that contains a more universal form of the name. (ANSI)
helpviewer_keywords: ["REMOTE_NAME_INFO_LEVEL", "UNIVERSAL_NAME_INFO_LEVEL", "WNetGetUniversalNameA", "winnetwk/WNetGetUniversalNameA"]
old-location: wnet\wnetgetuniversalname.htm
tech.root: WNet
ms.assetid: 12c02092-f2d5-4477-92a7-ae075b8a243a
ms.date: 12/05/2018
ms.keywords: REMOTE_NAME_INFO_LEVEL, UNIVERSAL_NAME_INFO_LEVEL, WNetGetUniversalName, WNetGetUniversalName function [Windows Networking (WNet)], WNetGetUniversalNameA, WNetGetUniversalNameW, _win32_wnetgetuniversalname, winnetwk/WNetGetUniversalName, winnetwk/WNetGetUniversalNameA, winnetwk/WNetGetUniversalNameW, wnet.wnetgetuniversalname
req.header: winnetwk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WNetGetUniversalNameW (Unicode) and WNetGetUniversalNameA (ANSI)
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
 - WNetGetUniversalNameA
 - winnetwk/WNetGetUniversalNameA
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
 - WNetGetUniversalName
 - WNetGetUniversalNameA
 - WNetGetUniversalNameW
---

# WNetGetUniversalNameA function


## -description

The
				<b>WNetGetUniversalName</b> function takes a drive-based path for a network resource and returns an information structure that contains a more universal form of the name.

## -parameters

### -param lpLocalPath [in]

A pointer to a constant null-terminated string that is a drive-based path for a network resource. 




For example, if drive H has been mapped to a network drive share, and the network       resource of interest is a file named Sample.doc in the directory \Win32\Examples on that share, the drive-based path is H:\Win32\Examples\Sample.doc.

### -param dwInfoLevel [in]

The type of structure that the function stores in the buffer pointed to by the <i>lpBuffer</i> parameter. This parameter can be one of the following values defined in the <i>Winnetwk.h</i> header file.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="UNIVERSAL_NAME_INFO_LEVEL"></a><a id="universal_name_info_level"></a><dl>
<dt><b>UNIVERSAL_NAME_INFO_LEVEL</b></dt>
</dl>
</td>
<td width="60%">
The function stores a 
<a href="/windows/desktop/api/winnetwk/ns-winnetwk-universal_name_infoa">UNIVERSAL_NAME_INFO</a> structure in the buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="REMOTE_NAME_INFO_LEVEL"></a><a id="remote_name_info_level"></a><dl>
<dt><b>REMOTE_NAME_INFO_LEVEL</b></dt>
</dl>
</td>
<td width="60%">
The function stores a 
<a href="/windows/desktop/api/winnetwk/ns-winnetwk-remote_name_infow">REMOTE_NAME_INFO</a> structure in the buffer.

</td>
</tr>
</table>
 

The 
<a href="/windows/desktop/api/winnetwk/ns-winnetwk-universal_name_infoa">UNIVERSAL_NAME_INFO</a> structure points to a Universal Naming Convention (UNC) name string.

The 
<a href="/windows/desktop/api/winnetwk/ns-winnetwk-remote_name_infow">REMOTE_NAME_INFO</a> structure points to a UNC name string and two additional connection information strings. For more information, see the following Remarks section.

### -param lpBuffer [out]

A pointer to a buffer that receives the structure specified by the <i>dwInfoLevel</i> parameter.

### -param lpBufferSize [in, out]

A pointer to a variable that specifies the size, in bytes, of the buffer pointed to by the <i>lpBuffer</i> parameter.

If the function succeeds, it sets the variable pointed to by <i>lpBufferSize</i> to the number of bytes stored in the buffer. If the function fails because the buffer is too small, this location receives the required buffer size, and the function returns ERROR_MORE_DATA.

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
<dt><b>ERROR_BAD_DEVICE</b></dt>
</dl>
</td>
<td width="60%">
The string pointed to by the <i>lpLocalPath</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CONNECTION_UNAVAIL</b></dt>
</dl>
</td>
<td width="60%">
There is no current connection to the remote device, but there is a remembered (persistent) connection to it.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_EXTENDED_ERROR</b></dt>
</dl>
</td>
<td width="60%">
A network-specific error occurred. Use the 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetlasterrora">WNetGetLastError</a> function to obtain a description of the error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by the <i>lpBuffer</i> parameter is too small. The function sets the variable pointed to by the <i>lpBufferSize</i> parameter to the required buffer size. More entries are available with subsequent calls.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwInfoLevel</i> parameter is set to UNIVERSAL_NAME_INFO_LEVEL, but the network provider does not support UNC names. (None of the network providers support this function.)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_NET_OR_BAD_PATH</b></dt>
</dl>
</td>
<td width="60%">
None of the network providers recognize the local name as having a connection. However, the network is not available for at least one provider to whom the connection may belong.

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
<dt><b>ERROR_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The device specified by the <i>lpLocalPath</i> parameter is not redirected.

</td>
</tr>
</table>

## -remarks

A universal form of a local drive-based path identifies a network resource in an unambiguous, computer-independent manner. The name can then be passed to processes on other computers, allowing those processes to obtain access to the resource.

The 
<b>WNetGetUniversalName</b> function currently supports one universal name form: universal naming convention (UNC) names, which look like the following:


``` syntax
\\servername\sharename\path\file 

```

Using the example from the preceding description of the <i>lpLocalPath</i> parameter, if the shared network drive is on a server named COOLSERVER, and the share name is HOTSHARE, the UNC name for the network resource whose drive-based name is H:\Win32\Examples\Sample.doc would be the following:


``` syntax
\\coolserver\hotshare\win32\examples\sample.doc 

```

The 
<a href="/windows/desktop/api/winnetwk/ns-winnetwk-universal_name_infoa">UNIVERSAL_NAME_INFO</a> structure contains a pointer to a UNC name string. The 
<a href="/windows/desktop/api/winnetwk/ns-winnetwk-remote_name_infow">REMOTE_NAME_INFO</a> structure also contains a pointer to a UNC name string as well as pointers to two other useful strings. For example, a process can pass the 
<b>REMOTE_NAME_INFO</b> structure's <b>lpszConnectionInfo</b> member to the 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a">WNetAddConnection2</a> function to connect a local device to the network resource. Then the process can append the string pointed to by the <b>lpszRemainingPath</b> member to the local device string. The resulting string can be passed to functions that require a drive-based path.

The <i>lpLocalPath</i> parameter does not have to specify a path or resource that is already present on a remote resource.  For example, the <i>lpLocalPath</i> parameter could specify and folder, a hierarchy of folders, or a file that does not currently exist. The
				<b>WNetGetUniversalName</b> function returns a more universal form of the name in these cases.

The size of the buffer pointed to by the <i>lpBuffer</i> parameter and specified in the <i>lpBufferSize</i> parameter must be much larger than the size of the <a href="/windows/desktop/api/winnetwk/ns-winnetwk-remote_name_infow">REMOTE_NAME_INFO</a> 
		 or <a href="/windows/desktop/api/winnetwk/ns-winnetwk-universal_name_infoa">UNIVERSAL_NAME_INFO</a> structures. The buffer pointed to by the <i>lpBuffer</i> parameter must be large enough to store the UNC strings pointed to by the members in the <b>REMOTE_NAME_INFO</b> 
		 or <b>UNIVERSAL_NAME_INFO</b> structures. If the buffer size is too small, then the function fails with ERROR_MORE_DATA and the variable pointed to by the <i>lpBufferSize</i> parameter indicates the required buffer size.

<b>Windows Server 2003 and Windows XP:  </b>This function queries the MS-DOS device namespaces associated with a logon session because MS-DOS devices are identified by AuthenticationID. (An AuthenticationID is the 
<a href="/windows/desktop/SecGloss/l-gly">locally unique identifier</a>, or LUID, associated with a logon session.) This can affect applications that call one of the WNet functions to create a network drive letter under one user logon, but query for existing network drive letters under a different user logon. An example of this situation could be when a user's second logon is created within a logon session, for example, by calling the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a> function, and the second logon runs an application that calls the 
<a href="/windows/desktop/api/fileapi/nf-fileapi-getlogicaldrives">GetLogicalDrives</a> function. <b>GetLogicalDrives</b> does not return network drive letters created by a WNet function under the first logon. Note that in the preceding example the first logon session still exists, and the example could apply to any logon session, including a Terminal Services session. For more information, see 
<a href="/windows/desktop/FileIO/defining-an-ms-dos-device-name">Defining an MS-DOS Device Name</a>.


#### Examples

The following code sample illustrates how to use the 
<b>WNetGetUniversalName</b> function to retrieve the universal UNC name strings associated with drive-based path for a network resource.


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

    WCHAR Buffer[1024];
    DWORD dwBufferLength = 1024;
       
    UNIVERSAL_NAME_INFO * unameinfo;
    REMOTE_NAME_INFO *remotenameinfo;
    
    wprintf(L"Calling WNetGetUniversalName with Local Path = %s\n", argv[1]);

    unameinfo = (UNIVERSAL_NAME_INFO *) &Buffer;
    dwRetVal = WNetGetUniversalName(argv[1], UNIVERSAL_NAME_INFO_LEVEL, (LPVOID) unameinfo, &dwBufferLength );
    //
    // If the call succeeds, print the user information.
    //
    if (dwRetVal == NO_ERROR) {

        wprintf(L"WNetGetUniversalName returned success for InfoLevel=UNIVERSAL_NAME_INFO_LEVEL\n");
        wprintf(L"\tUniversal name = %s\n", unameinfo->lpUniversalName);
    }

    else {
        wprintf(L"WNetGetUser failed for InfoLevel=UNIVERSAL_NAME_INFO_LEVEL with error: %u\n", dwRetVal);
    }


    remotenameinfo = (REMOTE_NAME_INFO *) &Buffer;
    dwRetVal = WNetGetUniversalName(argv[1], REMOTE_NAME_INFO_LEVEL, 
        (LPVOID) remotenameinfo, &dwBufferLength );
    //
    // If the call succeeds, print the user information.
    //
    if (dwRetVal == NO_ERROR) {

        wprintf(L"WNetGetUniversalName returned success for InfoLevel=REMOTE_NAME_INFO_LEVEL\n");
        wprintf(L"\tUniversal name = %s\n", remotenameinfo->lpUniversalName);
        wprintf(L"\tConnection name = %s\n", remotenameinfo->lpConnectionName);
        wprintf(L"\tRemaining path = %s\n", remotenameinfo->lpRemainingPath);
    }

    else {
        wprintf(L"WNetGetUser failed for InfoLevel=REMOTE_NAME_INFO_LEVEL with error: %u\n", dwRetVal);
    }
}


```






> [!NOTE]
> The winnetwk.h header defines WNetGetUniversalName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WNet/determining-the-location-of-a-share">Determining the Location of a Share</a>



<a href="/windows/desktop/api/winnetwk/ns-winnetwk-remote_name_infow">REMOTE_NAME_INFO</a>



<a href="/windows/desktop/api/winnetwk/ns-winnetwk-universal_name_infoa">UNIVERSAL_NAME_INFO</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a">WNetAddConnection2</a>



<a href="/windows/desktop/WNet/windows-networking-wnet-">Windows
		  Networking (WNet) Overview</a>



<a href="/windows/desktop/WNet/windows-networking-functions">Windows
		  Networking Functions</a>
