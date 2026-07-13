---
UID: NF:winnetwk.WNetGetConnectionA
title: WNetGetConnectionA function (winnetwk.h)
description: The WNetGetConnection function retrieves the name of the network resource associated with a local device. (ANSI)
helpviewer_keywords: ["WNetGetConnectionA", "winnetwk/WNetGetConnectionA"]
old-location: wnet\wnetgetconnection.htm
tech.root: WNet
ms.assetid: 72d84752-4e64-4c16-872b-cb892dffbf9a
ms.date: 12/05/2018
ms.keywords: WNetGetConnection, WNetGetConnection function [Windows Networking (WNet)], WNetGetConnectionA, WNetGetConnectionW, _win32_wnetgetconnection, winnetwk/WNetGetConnection, winnetwk/WNetGetConnectionA, winnetwk/WNetGetConnectionW, wnet.wnetgetconnection
req.header: winnetwk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WNetGetConnectionW (Unicode) and WNetGetConnectionA (ANSI)
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
 - WNetGetConnectionA
 - winnetwk/WNetGetConnectionA
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
 - WNetGetConnection
 - WNetGetConnectionA
 - WNetGetConnectionW
---

# WNetGetConnectionA function


## -description

The
				<b>WNetGetConnection</b> function retrieves the name of the network resource associated with a local device.

## -parameters

### -param lpLocalName [in]

Pointer to a constant null-terminated string that specifies the name of the local device to get the network name for.

### -param lpRemoteName [out]

Pointer to a null-terminated  string  that receives the remote name used to make the connection.

### -param lpnLength [in, out]

Pointer to a variable that specifies the size of the buffer pointed to by the <i>lpRemoteName</i> parameter, in characters. If the function fails because the buffer is not large enough, this parameter returns the required buffer size.

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
The string pointed to by the <i>lpLocalName</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The device specified by <i>lpLocalName</i> is not a redirected device. For more information, see the following Remarks section.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The buffer is too small. The <i>lpnLength</i> parameter points to a variable that contains the required buffer size. More entries are available with subsequent calls.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CONNECTION_UNAVAIL</b></dt>
</dl>
</td>
<td width="60%">
The device is not currently connected, but it is a persistent connection. For more information, see the following Remarks section.

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

If the network connection was made using the Microsoft LAN Manager network, and the calling application is running in a different logon session than the application that made the connection, a call to the 
<b>WNetGetConnection</b> function for the associated local device will fail. The function fails with ERROR_NOT_CONNECTED or ERROR_CONNECTION_UNAVAIL. This is because a connection made using Microsoft LAN Manager is visible only to applications running in the same logon session as the application that made the connection. (To prevent the call to 
<b>WNetGetConnection</b> from failing it is not sufficient for the application to be running in the user account that created the connection.)

<b>Windows Server 2003 and Windows XP:  </b>This function queries the MS-DOS device namespaces associated with a logon session because MS-DOS devices are identified by AuthenticationID. (An AuthenticationID is the 
<a href="/windows/desktop/SecGloss/l-gly">locally unique identifier</a>, or LUID, associated with a logon session.) This can affect applications that call one of the WNet functions to create a network drive letter under one user logon, but query for existing network drive letters under a different user logon. An example of this situation could be when a user's second logon is created within a logon session, for example, by calling the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a> function, and the second logon runs an application that calls the 
<a href="/windows/desktop/api/fileapi/nf-fileapi-getlogicaldrives">GetLogicalDrives</a> function. <b>GetLogicalDrives</b> does not return network drive letters created by a WNet function under the first logon. Note that in the preceding example the first logon session still exists, and the example could apply to any logon session, including a Terminal Services session. For more information, see 
<a href="/windows/desktop/FileIO/defining-an-ms-dos-device-name">Defining an MS-DOS Device Name</a>.


#### Examples

For a code sample that illustrates how to use the 
<b>WNetGetConnection</b> function to retrieve the name of the network resource associated with a local device, see 
<a href="/windows/desktop/WNet/retrieving-the-connection-name">Retrieving the Connection Name</a>.

<div class="code"></div>




> [!NOTE]
> The winnetwk.h header defines WNetGetConnection as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a">WNetAddConnection2</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection3a">WNetAddConnection3</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetusera">WNetGetUser</a>



<a href="/windows/desktop/WNet/windows-networking-wnet-">Windows
		  Networking (WNet) Overview</a>



<a href="/windows/desktop/WNet/windows-networking-functions">Windows
		  Networking Functions</a>
