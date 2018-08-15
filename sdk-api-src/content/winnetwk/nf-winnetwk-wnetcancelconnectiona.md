---
UID: NF:winnetwk.WNetCancelConnectionA
title: WNetCancelConnectionA function
author: windows-sdk-content
description: The WNetCancelConnection function cancels an existing network connection.
old-location: wnet\wnetcancelconnection.htm
old-project: wnet
ms.assetid: e180d497-5e14-459a-8cf6-5664dfb88419
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WNetCancelConnection, WNetCancelConnection function [Windows Networking (WNet)], WNetCancelConnectionA, WNetCancelConnectionW, _win32_wnetcancelconnection, winnetwk/WNetCancelConnection, winnetwk/WNetCancelConnectionA, winnetwk/WNetCancelConnectionW, wnet.wnetcancelconnection
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
req.unicode-ansi: WNetCancelConnectionW (Unicode) and WNetCancelConnectionA (ANSI)
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
 - WNetCancelConnection
 - WNetCancelConnectionA
 - WNetCancelConnectionW
product: Windows
targetos: Windows
req.lib: Mpr.lib
req.dll: Mpr.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WNetCancelConnectionA function


## -description


The
				<b>WNetCancelConnection</b> function cancels an existing network connection.

The 
<b>WNetCancelConnection</b> function is provided for compatibility with 16-bit versions of Windows. Other Windows-based applications should call the 
<a href="https://msdn.microsoft.com/8bb8222f-6ede-4bf4-a6e4-681560cce162">WNetCancelConnection2</a> function.


## -parameters




### -param lpName [in]

Pointer to a constant null-terminated string that specifies the name of either the redirected local device or the remote network resource to disconnect from. 




When this parameter specifies a redirected local device, the function cancels only the specified device redirection. If the parameter specifies a remote network resource, only the connections to remote networks without devices are canceled.


### -param fForce [in]

Specifies whether or not the disconnection should occur if there are open files or jobs on the connection. If this parameter is <b>FALSE</b>, the function fails if there are open files or jobs.


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
<a href="https://msdn.microsoft.com/8e13c467-adcf-4e97-b51a-1f5fc919b51e">WNetGetLastError</a> function.

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
<a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">locally unique identifier</a>, or LUID, associated with a logon session.) This can affect applications that call one of the WNet functions to create a network drive letter under one user logon, but query for existing network drive letters under a different user logon. An example of this situation could be when a user's second logon is created within a logon session, for example, by calling the 
<a href="https://msdn.microsoft.com/6b3f4dd9-500b-420e-804a-401a9e188be8">CreateProcessAsUser</a> function, and the second logon runs an application that calls the 
<a href="https://msdn.microsoft.com/21a66050-3bab-4c70-9003-3b52e8c72b00">GetLogicalDrives</a> function. <b>GetLogicalDrives</b> does not return network drive letters created by a WNet function under the first logon. Note that in the preceding example the first logon session still exists, and the example could apply to any logon session, including a Terminal Services session. For more information, see 
<a href="https://msdn.microsoft.com/7d802e9f-dc09-4e3d-b064-e9b57af396e2">Defining an MS-DOS Device Name</a>.




## -see-also




<a href="https://msdn.microsoft.com/9f2cf166-eb08-4498-8cda-79808776a452">WNetAddConnection</a>



<a href="https://msdn.microsoft.com/faec728c-f19e-418c-9bdb-cde93e7d98fb">WNetAddConnection2</a>



<a href="https://msdn.microsoft.com/8bb8222f-6ede-4bf4-a6e4-681560cce162">WNetCancelConnection2</a>



<a href="https://msdn.microsoft.com/72d84752-4e64-4c16-872b-cb892dffbf9a">WNetGetConnection</a>



<a href="https://msdn.microsoft.com/7668ac55-7104-4ddb-88eb-920cfe4e36fd">Windows
		  Networking (WNet) Overview</a>



<a href="https://msdn.microsoft.com/95e30f8f-a326-424d-bd80-5fc9b3078dad">Windows
		  Networking Functions</a>
 

 

