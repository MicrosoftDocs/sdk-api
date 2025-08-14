---
UID: NF:winnetwk.WNetUseConnectionA
title: WNetUseConnectionA function (winnetwk.h)
description: The WNetUseConnection function makes a connection to a network resource. The function can redirect a local device to a network resource. (ANSI)
helpviewer_keywords: ["CONNECT_CMD_SAVECRED", "CONNECT_COMMANDLINE", "CONNECT_INTERACTIVE", "CONNECT_LOCALDRIVE", "CONNECT_PROMPT", "CONNECT_REDIRECT", "CONNECT_UPDATE_PROFILE", "WNetUseConnectionA", "dwType", "lpLocalName", "lpProvider", "lpRemoteName", "winnetwk/WNetUseConnectionA"]
old-location: wnet\wnetuseconnection.htm
tech.root: WNet
ms.assetid: 80fa471d-074c-468f-b90f-1636081e1583
ms.date: 12/05/2018
ms.keywords: CONNECT_CMD_SAVECRED, CONNECT_COMMANDLINE, CONNECT_INTERACTIVE, CONNECT_LOCALDRIVE, CONNECT_PROMPT, CONNECT_REDIRECT, CONNECT_UPDATE_PROFILE, WNetUseConnection, WNetUseConnection function [Windows Networking (WNet)], WNetUseConnectionA, WNetUseConnectionW, _win32_wnetuseconnection, dwType, lpLocalName, lpProvider, lpRemoteName, winnetwk/WNetUseConnection, winnetwk/WNetUseConnectionA, winnetwk/WNetUseConnectionW, wnet.wnetuseconnection
req.header: winnetwk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WNetUseConnectionW (Unicode) and WNetUseConnectionA (ANSI)
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
 - WNetUseConnectionA
 - winnetwk/WNetUseConnectionA
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
 - WNetUseConnection
 - WNetUseConnectionA
 - WNetUseConnectionW
---

# WNetUseConnectionA function


## -description

The
				<b>WNetUseConnection</b> function makes a connection to a network resource. The function can redirect a local device to a network resource.

The 
<b>WNetUseConnection</b> function is similar to the 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection3a">WNetAddConnection3</a> function. The main difference is that 
<b>WNetUseConnection</b> can automatically select an unused local device to redirect to the network resource.

## -parameters

### -param hwndOwner [in]

Handle to a window that the provider of network resources can use as an owner window for dialog boxes. Use this parameter if you set the CONNECT_INTERACTIVE value in the <i>dwFlags</i> parameter.

### -param lpNetResource [in]

Pointer to a <a href="ns-winnetwk-netresourcea.md">NETRESOURCE</a> structure that specifies details of the proposed connection. The structure contains information about the network resource, the local device, and the network resource provider. 




You must specify the following members of the 
<b>NETRESOURCE</b> structure.

<table>
<tr>
<th>Member</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="dwType"></a><a id="dwtype"></a><a id="DWTYPE"></a><dl>
<dt><b><b>dwType</b></b></dt>
</dl>
</td>
<td width="60%">
Specifies the type of resource to connect to. 




It is most efficient to specify a resource type in this member, such as RESOURCETYPE_DISK or RESOURCETYPE_PRINT. However, if the <b>lpLocalName</b> member is <b>NULL</b>, or if it points to an empty string and CONNECT_REDIRECT is not set, <b>dwType</b> can be RESOURCETYPE_ANY.

This method works only if the function does not automatically choose a device to redirect to the network resource.

Although this member is required, its information may be ignored by the network service provider.

</td>
</tr>
<tr>
<td width="40%"><a id="lpLocalName"></a><a id="lplocalname"></a><a id="LPLOCALNAME"></a><dl>
<dt><b><b>lpLocalName</b></b></dt>
</dl>
</td>
<td width="60%">
Pointer to a <b>null</b>-terminated string that specifies the name of a local device to be redirected, such as "F:" or "LPT1". The string is treated in a case-insensitive manner. 




If the string is empty, or if <b>lpLocalName</b> is <b>NULL</b>, a connection to the network occurs without redirection.

If the CONNECT_REDIRECT value is set in the <i>dwFlags</i> parameter, or if the network requires a redirected local device, the function chooses a local device to redirect and returns the name of the device in the <i>lpAccessName</i> parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="lpRemoteName"></a><a id="lpremotename"></a><a id="LPREMOTENAME"></a><dl>
<dt><b><b>lpRemoteName</b></b></dt>
</dl>
</td>
<td width="60%">
Pointer to a <b>null</b>-terminated string that specifies the network resource to connect to. The string can be up to MAX_PATH characters in length, and it must follow the network provider's naming conventions.

</td>
</tr>
<tr>
<td width="40%"><a id="lpProvider"></a><a id="lpprovider"></a><a id="LPPROVIDER"></a><dl>
<dt><b><b>lpProvider</b></b></dt>
</dl>
</td>
<td width="60%">
Pointer to a <b>null</b>-terminated string that specifies the network provider to connect to. If <b>lpProvider</b> is <b>NULL</b>, or if it points to an empty string, the operating system attempts to determine the correct provider by parsing the string pointed to by the <b>lpRemoteName</b> member. 




If this member is not <b>NULL</b>, the operating system attempts to make a connection only to the named network provider.

You should set this member only if you know the network provider you want to use. Otherwise, let the operating system determine which provider the network name maps to.

</td>
</tr>
</table>
 

The 
<b>WNetUseConnection</b> function ignores the other members of the 
<a href="ns-winnetwk-netresourcea.md">NETRESOURCE</a> structure. For more information, see the descriptions following for the <i>dwFlags</i> parameter.

### -param lpPassword [in]

Pointer to a constant <b>null</b>-terminated string that specifies a password to be used in making the network connection. 




If <i>lpPassword</i> is <b>NULL</b>, the function uses the current default password associated with the user specified by <i>lpUserID</i>.
						

If <i>lpPassword</i> points to an empty string, the function does not use a password.

If the connection fails because of an invalid password and the CONNECT_INTERACTIVE value is set in the <i>dwFlags</i> parameter, the function displays a dialog box asking the user to type the password.

### -param lpUserId [in]

Pointer to a constant <b>null</b>-terminated string that specifies a user name for making the connection. 




If <i>lpUserID</i> is <b>NULL</b>, the function uses the default user name. (The user context for the process provides the default user name.)

The <i>lpUserID</i> parameter is specified when users want to connect to a network resource for which they have been assigned a user name or account other than the default user name or account.

The user-name string represents a 
<a href="/windows/desktop/SecGloss/s-gly">security context</a>. It may be specific to a network provider.

### -param dwFlags [in]

Set of bit flags describing the connection. This parameter can be any combination of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CONNECT_INTERACTIVE"></a><a id="connect_interactive"></a><dl>
<dt><b>CONNECT_INTERACTIVE</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the operating system may interact with the user for authentication purposes.

</td>
</tr>
<tr>
<td width="40%"><a id="CONNECT_PROMPT"></a><a id="connect_prompt"></a><dl>
<dt><b>CONNECT_PROMPT</b></dt>
</dl>
</td>
<td width="60%">
This flag instructs the system not to use any default settings for user names or passwords without offering the user the opportunity to supply an alternative. This flag is ignored unless CONNECT_INTERACTIVE is also set.

</td>
</tr>
<tr>
<td width="40%"><a id="CONNECT_REDIRECT"></a><a id="connect_redirect"></a><dl>
<dt><b>CONNECT_REDIRECT</b></dt>
</dl>
</td>
<td width="60%">
This flag forces the redirection of a local device when making the connection. 




If the <b>lpLocalName</b> member of 
<a href="ns-winnetwk-netresourcea.md">NETRESOURCE</a> specifies a local device to redirect, this flag has no effect, because the operating system still attempts to redirect the specified device. When the operating system automatically chooses a local device, the <b>dwType</b> member must not be equal to RESOURCETYPE_ANY.

If this flag is not set, a local device is automatically chosen for redirection only if the network requires a local device to be redirected.

<b>Windows XP:  </b>When the system automatically assigns network drive letters, letters are assigned beginning with Z:, then Y:, and ending with C:. This reduces collision between per-logon drive letters (such as network drive letters) and global drive letters (such as disk drives). Note that previous releases assigned drive letters beginning with C: and ending with Z:.

</td>
</tr>
<tr>
<td width="40%"><a id="CONNECT_UPDATE_PROFILE"></a><a id="connect_update_profile"></a><dl>
<dt><b>CONNECT_UPDATE_PROFILE</b></dt>
</dl>
</td>
<td width="60%">
This flag instructs the operating system to store the network resource connection. 




If this bit flag is set, the operating system automatically attempts to restore the connection when the user logs on. The system remembers only successful connections that redirect local devices. It does not remember connections that are unsuccessful or deviceless connections. (A deviceless connection occurs when <b>lpLocalName</b> is <b>NULL</b> or when it points to an empty string.)

If this bit flag is clear, the operating system does not automatically restore the connection at logon.

</td>
</tr>
<tr>
<td width="40%"><a id="CONNECT_COMMANDLINE"></a><a id="connect_commandline"></a><dl>
<dt><b>CONNECT_COMMANDLINE</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the operating system prompts the user for authentication using the command line instead of a graphical user interface (GUI). This flag is ignored unless CONNECT_INTERACTIVE is also set.

<b>Windows 2000/NT and Windows Me/98/95:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="CONNECT_CMD_SAVECRED"></a><a id="connect_cmd_savecred"></a><dl>
<dt><b>CONNECT_CMD_SAVECRED</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, and the operating system prompts for a credential, the credential should be saved by the credential manager. If the credential manager is disabled for the caller's logon session, or if the network provider does not support saving credentials, this flag is ignored. This flag is also ignored unless you set the CONNECT_COMMANDLINE flag.

<b>Windows 2000/NT and Windows Me/98/95:  </b>This value is not supported.

</td>
</tr>
</table>

### -param lpAccessName [out]

Pointer to a buffer that receives system requests on the connection. This parameter can be <b>NULL</b>. 




If this parameter is specified, and the <b>lpLocalName</b> member of the 
<b>NETRESOURCE</b> structure specifies a local device, this buffer receives the local device name. If <b>lpLocalName</b> does not specify a device and the network requires a local device redirection, or if the CONNECT_REDIRECT value is set, this buffer receives the name of the redirected local device.

Otherwise, the name copied into the buffer is that of a remote resource. If specified, this buffer must be at least as large as the string pointed to by the <b>lpRemoteName</b> member.

### -param lpBufferSize [in, out]

Pointer to a variable that specifies the size of the <i>lpAccessName</i> buffer, in characters. If the call fails because the buffer is not large enough, the function returns the required buffer size in this location. For more information, see the descriptions of the <i>lpAccessName</i> parameter and the ERROR_MORE_DATA error code in the Return Values section.

### -param lpResult [out]

Pointer to a variable that receives additional information about the connection. This parameter can be the following value. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CONNECT_LOCALDRIVE"></a><a id="connect_localdrive"></a><dl>
<dt><b>CONNECT_LOCALDRIVE</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the connection was made using a local device redirection. If the <i>lpAccessName</i> parameter points to a buffer, the local device name is copied to the buffer.

</td>
</tr>
</table>

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
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have access to the network resource.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ALREADY_ASSIGNED</b></dt>
</dl>
</td>
<td width="60%">
The local device specified by the <b>lpLocalName</b> member is already connected to a network resource.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_DEVICE</b></dt>
</dl>
</td>
<td width="60%">
The value specified by <b>lpLocalName</b> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_NET_NAME</b></dt>
</dl>
</td>
<td width="60%">
The value specified by the <b>lpRemoteName</b> member is not acceptable to any network resource provider because the resource name is invalid, or because the named resource cannot be located.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_PROVIDER</b></dt>
</dl>
</td>
<td width="60%">
The value specified by the <b>lpProvider</b> member does not match any provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The attempt to make the connection was canceled by the user through a dialog box from one of the network resource providers, or by a called resource.

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
<dt><b>ERROR_INVALID_ADDRESS</b></dt>
</dl>
</td>
<td width="60%">
The caller passed in a pointer to a buffer that could not be accessed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
This error is a result of one of the following conditions: 




<ol>
<li>The <b>lpRemoteName</b> member is <b>NULL</b>. In addition, <i>lpAccessName</i> is not <b>NULL</b>, but <i>lpBufferSize</i> is either <b>NULL</b> or points to zero.</li>
<li>The <b>dwType</b> member is neither RESOURCETYPE_DISK nor RESOURCETYPE_PRINT. In addition, either CONNECT_REDIRECT is set in <i>dwFlags</i> and <b>lpLocalName</b> is <b>NULL</b>, or the connection is to a network that requires the redirecting of a local device.</li>
</ol>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PASSWORD</b></dt>
</dl>
</td>
<td width="60%">
The specified password is invalid and the CONNECT_INTERACTIVE flag is not set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpAccessName</i> buffer is too small. 




If a local device is redirected, the buffer needs to be large enough to contain the local device name. Otherwise, the buffer needs to be large enough to contain either the string pointed to by <b>lpRemoteName</b>, or the name of the connectable resource whose alias is pointed to by <b>lpRemoteName</b>. If this error is returned, then no connection has been made.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
The operating system cannot automatically choose a local redirection because all the valid local devices are in use.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_NET_OR_BAD_PATH</b></dt>
</dl>
</td>
<td width="60%">
The operation could not be completed, either because a network component is not started, or because the specified resource name is not recognized.

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
</table>

## -remarks

<b>Windows Server 2003 and Windows XP:  </b>The WNet functions create and delete network drive letters in the MS-DOS device namespace associated with a logon session because MS-DOS devices are identified by AuthenticationID. (An AuthenticationID is the 
<a href="/windows/desktop/SecGloss/l-gly">locally unique identifier</a>, or LUID, associated with a logon session.) This can affect applications that call one of the WNet functions to create a network drive letter under one user logon, but query for existing network drive letters under a different user logon. An example of this situation could be when a user's second logon is created within a logon session, for example, by calling the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a> function, and the second logon runs an application that calls the 
<a href="/windows/desktop/api/fileapi/nf-fileapi-getlogicaldrives">GetLogicalDrives</a> function. <b>GetLogicalDrives</b> does not return network drive letters created by a WNet function under the first logon. Note that in the preceding example the first logon session still exists, and the example could apply to any logon session, including a Terminal Services session. For more information, see 
<a href="/windows/desktop/FileIO/defining-an-ms-dos-device-name">Defining an MS-DOS Device Name</a>.





> [!NOTE]
> The winnetwk.h header defines WNetUseConnection as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a">WNetAddConnection2</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection3a">WNetAddConnection3</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetconnectiona">WNetGetConnection</a>



<a href="/windows/desktop/WNet/windows-networking-wnet-">Windows
		  Networking (WNet) Overview</a>



<a href="/windows/desktop/WNet/windows-networking-functions">Windows
		  Networking Functions</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnectiona">WnetCancelConnection</a>
