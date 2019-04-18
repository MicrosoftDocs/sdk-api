---
UID: NF:winnetwk.WNetGetConnectionW
title: WNetGetConnectionW function (winnetwk.h)
author: windows-sdk-content
description: The WNetGetConnection function retrieves the name of the network resource associated with a local device.
old-location: wnet\wnetgetconnection.htm
tech.root: WNet
ms.assetid: 72d84752-4e64-4c16-872b-cb892dffbf9a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WNetGetConnection, WNetGetConnection function [Windows Networking (WNet)], WNetGetConnectionA, WNetGetConnectionW, _win32_wnetgetconnection, winnetwk/WNetGetConnection, winnetwk/WNetGetConnectionA, winnetwk/WNetGetConnectionW, wnet.wnetgetconnection
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WNetGetConnectionW function


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
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>, such as one of the following values.

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



If the network connection was made using the Microsoft LAN Manager network, and the calling application is running in a different logon session than the application that made the connection, a call to the 
<b>WNetGetConnection</b> function for the associated local device will fail. The function fails with ERROR_NOT_CONNECTED or ERROR_CONNECTION_UNAVAIL. This is because a connection made using Microsoft LAN Manager is visible only to applications running in the same logon session as the application that made the connection. (To prevent the call to 
<b>WNetGetConnection</b> from failing it is not sufficient for the application to be running in the user account that created the connection.)

<b>Windows Server 2003 and Windows XP:  </b>This function queries the MS-DOS device namespaces associated with a logon session because MS-DOS devices are identified by AuthenticationID. (An AuthenticationID is the 
<a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">locally unique identifier</a>, or LUID, associated with a logon session.) This can affect applications that call one of the WNet functions to create a network drive letter under one user logon, but query for existing network drive letters under a different user logon. An example of this situation could be when a user's second logon is created within a logon session, for example, by calling the 
<a href="https://msdn.microsoft.com/6b3f4dd9-500b-420e-804a-401a9e188be8">CreateProcessAsUser</a> function, and the second logon runs an application that calls the 
<a href="https://msdn.microsoft.com/21a66050-3bab-4c70-9003-3b52e8c72b00">GetLogicalDrives</a> function. <b>GetLogicalDrives</b> does not return network drive letters created by a WNet function under the first logon. Note that in the preceding example the first logon session still exists, and the example could apply to any logon session, including a Terminal Services session. For more information, see 
<a href="https://msdn.microsoft.com/7d802e9f-dc09-4e3d-b064-e9b57af396e2">Defining an MS-DOS Device Name</a>.


#### Examples

For a code sample that illustrates how to use the 
<b>WNetGetConnection</b> function to retrieve the name of the network resource associated with a local device, see 
<a href="https://msdn.microsoft.com/7c02cf9a-cca3-47d8-8a4b-f2245f1db92a">Retrieving the Connection Name</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/faec728c-f19e-418c-9bdb-cde93e7d98fb">WNetAddConnection2</a>



<a href="https://msdn.microsoft.com/169c7bb4-cb08-424c-af79-2133684a99db">WNetAddConnection3</a>



<a href="https://msdn.microsoft.com/8e73d2a9-c776-4661-81ab-84b7cf037cbd">WNetGetUser</a>



<a href="https://msdn.microsoft.com/7668ac55-7104-4ddb-88eb-920cfe4e36fd">Windows
		  Networking (WNet) Overview</a>



<a href="https://msdn.microsoft.com/95e30f8f-a326-424d-bd80-5fc9b3078dad">Windows
		  Networking Functions</a>
 

 

