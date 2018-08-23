---
UID: NF:winnetwk.WNetCancelConnection2A
title: WNetCancelConnection2A function
author: windows-sdk-content
description: The WNetCancelConnection2 function cancels an existing network connection. You can also call the function to remove remembered network connections that are not currently connected.
old-location: wnet\wnetcancelconnection2.htm
old-project: wnet
ms.assetid: 8bb8222f-6ede-4bf4-a6e4-681560cce162
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: 0, CONNECT_UPDATE_PROFILE, WNetCancelConnection2, WNetCancelConnection2 function [Windows Networking (WNet)], WNetCancelConnection2A, WNetCancelConnection2W, _win32_wnetcancelconnection2, winnetwk/WNetCancelConnection2, winnetwk/WNetCancelConnection2A, winnetwk/WNetCancelConnection2W, wnet.wnetcancelconnection2
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
req.unicode-ansi: WNetCancelConnection2W (Unicode) and WNetCancelConnection2A (ANSI)
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
 - WNetCancelConnection2
 - WNetCancelConnection2A
 - WNetCancelConnection2W
product: Windows
targetos: Windows
req.lib: Mpr.lib
req.dll: Mpr.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WNetCancelConnection2A function


## -description


The
				<b>WNetCancelConnection2</b> function cancels an existing network connection. You can also call the function to remove remembered network connections that are not currently connected.

The 
<b>WNetCancelConnection2</b> function supersedes the 
<a href="https://msdn.microsoft.com/e180d497-5e14-459a-8cf6-5664dfb88419">WNetCancelConnection</a> function.


## -parameters




### -param lpName [in]

Pointer to a constant <b>null</b>-terminated string that specifies the name of either the redirected local device or the remote network resource to disconnect from. 




If  this parameter specifies a redirected local device, the function cancels only the specified device redirection. If the parameter specifies a remote network resource, all connections without devices are canceled.


### -param dwFlags [in]

Connection type. The following values are defined. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
The system does not update information about the connection. 




If the connection was marked as persistent in the registry, the system continues to restore the connection at the next logon. If the connection was not marked as persistent, the function ignores the setting of the CONNECT_UPDATE_PROFILE flag.

</td>
</tr>
<tr>
<td width="40%"><a id="CONNECT_UPDATE_PROFILE"></a><a id="connect_update_profile"></a><dl>
<dt><b>CONNECT_UPDATE_PROFILE</b></dt>
</dl>
</td>
<td width="60%">
The system updates the user profile with the information that the connection is no longer a persistent one. 




The system will not restore this connection during subsequent logon operations. (Disconnecting resources using remote names has no effect on persistent connections.)

</td>
</tr>
</table>
 


### -param fForce [in]

Specifies whether the disconnection should occur if there are open files or jobs on the connection. If this parameter is <b>FALSE</b>, the function fails if there are open files or jobs.


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


#### Examples

For a code sample that illustrates how to cancel a connection to a network resource with a call to the 
<b>WNetCancelConnection2</b> function, see 
<a href="https://msdn.microsoft.com/a1c80222-4986-4c51-86a5-a1caacb4b2fe">Canceling a Network Connection</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/faec728c-f19e-418c-9bdb-cde93e7d98fb">WNetAddConnection2</a>



<a href="https://msdn.microsoft.com/169c7bb4-cb08-424c-af79-2133684a99db">WNetAddConnection3</a>



<a href="https://msdn.microsoft.com/72d84752-4e64-4c16-872b-cb892dffbf9a">WNetGetConnection</a>



<a href="https://msdn.microsoft.com/7668ac55-7104-4ddb-88eb-920cfe4e36fd">Windows
		  Networking (WNet) Overview</a>



<a href="https://msdn.microsoft.com/95e30f8f-a326-424d-bd80-5fc9b3078dad">Windows
		  Networking Functions</a>
 

 

