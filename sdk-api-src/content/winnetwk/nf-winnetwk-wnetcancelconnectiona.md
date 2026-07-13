---
UID: NF:winnetwk.WNetCancelConnectionA
title: WNetCancelConnectionA function (winnetwk.h)
description: The WNetCancelConnection function cancels an existing network connection. (ANSI)
helpviewer_keywords: ["WNetCancelConnectionA", "winnetwk/WNetCancelConnectionA"]
old-location: wnet\wnetcancelconnection.htm
tech.root: WNet
ms.assetid: e180d497-5e14-459a-8cf6-5664dfb88419
ms.date: 12/05/2018
ms.keywords: WNetCancelConnection, WNetCancelConnection function [Windows Networking (WNet)], WNetCancelConnectionA, WNetCancelConnectionW, _win32_wnetcancelconnection, winnetwk/WNetCancelConnection, winnetwk/WNetCancelConnectionA, winnetwk/WNetCancelConnectionW, wnet.wnetcancelconnection
req.header: winnetwk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WNetCancelConnectionW (Unicode) and WNetCancelConnectionA (ANSI)
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
 - WNetCancelConnectionA
 - winnetwk/WNetCancelConnectionA
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
 - WNetCancelConnection
 - WNetCancelConnectionA
 - WNetCancelConnectionW
---

# WNetCancelConnectionA function


## -description

The
				<b>WNetCancelConnection</b> function cancels an existing network connection.

The 
<b>WNetCancelConnection</b> function is provided for compatibility with 16-bit versions of Windows. Other Windows-based applications should call the 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnection2a">WNetCancelConnection2</a> function.

## -parameters

### -param lpName [in]

Pointer to a constant null-terminated string that specifies the name of either the redirected local device or the remote network resource to disconnect from. 




When this parameter specifies a redirected local device, the function cancels only the specified device redirection. If the parameter specifies a remote network resource, only the connections to remote networks without devices are canceled.

### -param fForce [in]

Specifies whether or not the disconnection should occur if there are open files or jobs on the connection. If this parameter is <b>FALSE</b>, the function fails if there are open files or jobs.

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
<dt><b>ERROR_BAD_PROFILE</b></dt>
</dl>
</td>
<td width="60%">
The user profile is in an incorrect format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANNOT_OPEN_PROFILE</b></dt>
</dl>
</td>
<td width="60%">
The system is unable to open the user profile to process persistent connections.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DEVICE_IN_USE</b></dt>
</dl>
</td>
<td width="60%">
The device is in use by an active process and cannot be disconnected.

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
<dt><b>ERROR_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The name specified by the <i>lpName</i> parameter is not a redirected device, or the system is not currently connected to the device specified by the parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OPEN_FILES</b></dt>
</dl>
</td>
<td width="60%">
There are open files, and the <i>fForce</i> parameter is <b>FALSE</b>.

</td>
</tr>
</table>

## -remarks

<b>Windows Server 2003 and Windows XP:  </b>The WNet functions create and delete network drive letters in the MS-DOS device namespace associated with a logon session because MS-DOS devices are identified by AuthenticationID. (An AuthenticationID is the 
<a href="/windows/desktop/SecGloss/l-gly">locally unique identifier</a>, or LUID, associated with a logon session.) This can affect applications that call one of the WNet functions to create a network drive letter under one user logon, but query for existing network drive letters under a different user logon. An example of this situation could be when a user's second logon is created within a logon session, for example, by calling the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a> function, and the second logon runs an application that calls the 
<a href="/windows/desktop/api/fileapi/nf-fileapi-getlogicaldrives">GetLogicalDrives</a> function. <b>GetLogicalDrives</b> does not return network drive letters created by a WNet function under the first logon. Note that in the preceding example the first logon session still exists, and the example could apply to any logon session, including a Terminal Services session. For more information, see 
<a href="/windows/desktop/FileIO/defining-an-ms-dos-device-name">Defining an MS-DOS Device Name</a>.





> [!NOTE]
> The winnetwk.h header defines WNetCancelConnection as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnectiona">WNetAddConnection</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a">WNetAddConnection2</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnection2a">WNetCancelConnection2</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetconnectiona">WNetGetConnection</a>



<a href="/windows/desktop/WNet/windows-networking-wnet-">Windows
		  Networking (WNet) Overview</a>



<a href="/windows/desktop/WNet/windows-networking-functions">Windows
		  Networking Functions</a>
