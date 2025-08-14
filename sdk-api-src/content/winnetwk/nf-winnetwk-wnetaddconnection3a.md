---
UID: NF:winnetwk.WNetAddConnection3A
title: WNetAddConnection3A function (winnetwk.h)
description: The WNetAddConnection3 function makes a connection to a network resource. The function can redirect a local device to the network resource. (ANSI)
helpviewer_keywords: ["CONNECT_CMD_SAVECRED", "CONNECT_COMMANDLINE", "CONNECT_INTERACTIVE", "CONNECT_PROMPT", "CONNECT_REDIRECT", "CONNECT_UPDATE_PROFILE", "WNetAddConnection3A", "dwType", "lpLocalName", "lpProvider", "lpRemoteName", "winnetwk/WNetAddConnection3A"]
old-location: wnet\wnetaddconnection3.htm
tech.root: WNet
ms.assetid: 169c7bb4-cb08-424c-af79-2133684a99db
ms.date: 12/05/2018
ms.keywords: CONNECT_CMD_SAVECRED, CONNECT_COMMANDLINE, CONNECT_INTERACTIVE, CONNECT_PROMPT, CONNECT_REDIRECT, CONNECT_UPDATE_PROFILE, WNetAddConnection3, WNetAddConnection3 function [Windows Networking (WNet)], WNetAddConnection3A, WNetAddConnection3W, _win32_wnetaddconnection3, dwType, lpLocalName, lpProvider, lpRemoteName, winnetwk/WNetAddConnection3, winnetwk/WNetAddConnection3A, winnetwk/WNetAddConnection3W, wnet.wnetaddconnection3
req.header: winnetwk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WNetAddConnection3W (Unicode) and WNetAddConnection3A (ANSI)
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
 - WNetAddConnection3A
 - winnetwk/WNetAddConnection3A
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
 - WNetAddConnection3
 - WNetAddConnection3A
 - WNetAddConnection3W
---

# WNetAddConnection3A function


## -description

The
				<b>WNetAddConnection3</b> function makes a connection to a network resource. The function can redirect a local device to the network resource.

The 
<b>WNetAddConnection3</b> function is similar to the 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a">WNetAddConnection2</a> function. The main difference is that 
<b>WNetAddConnection3</b> has an additional parameter, a handle to a window that the provider of network resources can use as an owner window for dialog boxes. The 
<b>WNetAddConnection2</b> function and the 
<b>WNetAddConnection3</b> function supersede the 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnectiona">WNetAddConnection</a> function.

## -parameters

### -param hwndOwner [in]

A handle to a window that the provider of network resources can use as an owner window for dialog boxes. Use this parameter if you set the CONNECT_INTERACTIVE value in the <i>dwFlags</i> parameter.

The <i>hwndOwner</i> parameter can be <b>NULL</b>. If it is, a call to 
<b>WNetAddConnection3</b> is equivalent to calling the 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a">WNetAddConnection2</a> function.

### -param lpNetResource [in]

A pointer to a <a href="ns-winnetwk-netresourcea.md">NETRESOURCE</a> structure that specifies details of the proposed connection, such as information about the network resource, the local device, and the network resource provider. 




You must specify the following members of the <a href="ns-winnetwk-netresourcea.md">NETRESOURCE</a> structure.

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
The type of network resource to connect to. 




If the <b>lpLocalName</b> member points to a nonempty string, this member can be equal to RESOURCETYPE_DISK or RESOURCETYPE_PRINT.

If <b>lpLocalName</b> is <b>NULL</b>, or if it points to an empty string, <b>dwType</b> can be equal to RESOURCETYPE_DISK, RESOURCETYPE_PRINT, or RESOURCETYPE_ANY.

Although this member is required, its information may be ignored by the network service provider.

</td>
</tr>
<tr>
<td width="40%"><a id="lpLocalName"></a><a id="lplocalname"></a><a id="LPLOCALNAME"></a><dl>
<dt><b><b>lpLocalName</b></b></dt>
</dl>
</td>
<td width="60%">
A pointer to a <b>null</b>-terminated string that specifies the name of a local device to redirect, such as "F:" or "LPT1". The string is treated in a case-insensitive manner.

If the string is empty or if <b>lpLocalName</b> is <b>NULL</b>, the function makes a connection to the network resource without redirecting a local device.

</td>
</tr>
<tr>
<td width="40%"><a id="lpRemoteName"></a><a id="lpremotename"></a><a id="LPREMOTENAME"></a><dl>
<dt><b><b>lpRemoteName</b></b></dt>
</dl>
</td>
<td width="60%">
A pointer to a <b>null</b>-terminated string that specifies the network resource to connect to. The string can be up to MAX_PATH characters in length, and must follow the network provider's naming conventions.

</td>
</tr>
<tr>
<td width="40%"><a id="lpProvider"></a><a id="lpprovider"></a><a id="LPPROVIDER"></a><dl>
<dt><b><b>lpProvider</b></b></dt>
</dl>
</td>
<td width="60%">
A pointer to a <b>null</b>-terminated string that specifies the network provider to connect to.

If <b>lpProvider</b> is <b>NULL</b>, or if it points to an empty string, the operating system attempts to determine the correct provider by parsing the string pointed to by the <b>lpRemoteName</b> member.

If this member is not <b>NULL</b>, the operating system attempts to make a connection only to the named network provider.

You should set this member only if you know which network provider you want to use. Otherwise, let the operating system determine which network provider the network name maps to.

</td>
</tr>
</table>
 

The 
<b>WNetAddConnection3</b> function ignores the other members of the 
<a href="ns-winnetwk-netresourcea.md">NETRESOURCE</a> structure.

### -param lpPassword [in]

A pointer to a <b>null</b>-terminated string that specifies a password to be used in making the network connection. 




If <i>lpPassword</i> is <b>NULL</b>, the function uses the current default password associated with the user specified by the <i>lpUserName</i> parameter.
						

If <i>lpPassword</i> points to an empty string, the function does not use a password.

If the connection fails because of an invalid password and the CONNECT_INTERACTIVE value is set in the <i>dwFlags</i> parameter, the function displays a dialog box asking the user to type the password.

<b>Windows Me/98/95:  </b>This parameter must be <b>NULL</b> or an empty string.

### -param lpUserName [in]

A pointer to a <b>null</b>-terminated string that specifies a user name for making the connection. 




If <i>lpUserName</i> is <b>NULL</b>, the function uses the default user name. (The user context for the process provides the default user name.)

The <i>lpUserName</i> parameter is specified when users want to connect to a network resource for which they have been assigned a user name or account other than the default user name or account.

The user-name string represents a 
<a href="/windows/desktop/SecGloss/s-gly">security context</a>. It may be specific to a network provider.

<b>Windows Me/98/95:  </b>This parameter must be <b>NULL</b> or an empty string.

### -param dwFlags [in]

A set of connection options. The following values are currently defined.

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

<b>Windows Server 2003 and Windows XP:  </b>When the system automatically assigns network drive letters, letters are assigned beginning with Z:, then Y:, and ending with C:. This reduces collision between per-logon drive letters (such as network drive letters) and global drive letters (such as disk drives). Note that earlier versions of Windows assigned drive letters beginning with C: and ending with Z:.

</td>
</tr>
<tr>
<td width="40%"><a id="CONNECT_UPDATE_PROFILE"></a><a id="connect_update_profile"></a><dl>
<dt><b>CONNECT_UPDATE_PROFILE</b></dt>
</dl>
</td>
<td width="60%">
The network resource connection should be remembered.

If this bit flag is set, the operating system automatically attempts to restore the connection when the user logs on.

The operating system remembers only successful connections that redirect local devices. It does not remember connections that are unsuccessful or deviceless connections. (A deviceless connection occurs when the <b>lpLocalName</b> member is <b>NULL</b> or when it points to an empty string.)

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
<dt><b>ERROR_BAD_DEV_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The type of local device and the type of network resource do not match.

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
The value specified by the <b>lpRemoteName</b> member is not acceptable to any network resource provider, either because the resource name is invalid, or because the named resource cannot be located.

</td>
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
<dt><b>ERROR_BUSY</b></dt>
</dl>
</td>
<td width="60%">
The router or provider is busy, possibly initializing. The caller should retry.

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
<dt><b>ERROR_DEVICE_ALREADY_REMEMBERED</b></dt>
</dl>
</td>
<td width="60%">
An entry for the device specified by the <b>lpLocalName</b> member is already in the user profile.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_EXTENDED_ERROR</b></dt>
</dl>
</td>
<td width="60%">
A network-specific error occurred. Call the 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetlasterrora">WNetGetLastError</a> function to obtain a description of the error.

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
<dt><b>ERROR_NO_NET_OR_BAD_PATH</b></dt>
</dl>
</td>
<td width="60%">
The operation cannot be performed because a network component is not started or because a specified name cannot be used.

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

The 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetuseconnectiona">WNetUseConnection</a> function is similar to the 
<b>WNetAddConnection3</b> function. The main difference is that 
<b>WNetUseConnection</b> can automatically select an unused local device to redirect to the network resource.

On Windows Server 2003 and Windows XP, the WNet functions create and delete network drive letters in the MS-DOS device namespace associated with a logon session because MS-DOS devices are identified by AuthenticationID (a  
<a href="/windows/desktop/SecGloss/l-gly">locally unique identifier</a>, or LUID, associated with a logon session.) This can affect applications that call one of the WNet functions to create a network drive letter under one user logon, but query for existing network drive letters under a different user logon. An example of this situation could be when a user's second logon is created within a logon session, for example, by calling the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a> function, and the second logon runs an application that calls the 
<a href="/windows/desktop/api/fileapi/nf-fileapi-getlogicaldrives">GetLogicalDrives</a> function. The call to the <b>GetLogicalDrives</b> function does not return network drive letters created by WNet function calls under the first logon. Note that in the preceding example the first logon session still exists, and the example could apply to any logon session, including a Terminal Services session. For more information, see 
<a href="/windows/desktop/FileIO/defining-an-ms-dos-device-name">Defining an MS-DOS Device Name</a>.

On Windows Server 2003 and Windows XP, if a service that runs as LocalSystem calls the <b>WNetAddConnection3</b> function, then the mapped drive is visible to all user logon sessions.  

For Microsoft network providers, the <b>lpRemoteName</b> member of the <a href="ns-winnetwk-netresourcea.md">NETRESOURCE</a> structure pointed to by the <i>lpNetResource</i> parameter can contain an IPv4 address in dotted-decimal notation. An example for a share might be the following:

<code>\\192.168.1.1\share
</code>

For Microsoft network providers on Windows Vista and later, the <b>lpRemoteName</b> member of the <a href="ns-winnetwk-netresourcea.md">NETRESOURCE</a> structure pointed to by the <i>lpNetResource</i> parameter can contain an IPv6 address. However, the IPv6 literal format must be used so that the IPv6 address is parsed correctly. An IPv6 literal address is of the form:

ipv6-address with the ':' characters replaced by '-' characters followed by the ".ipv6-literal.net" string.


For example, for the following IPv6 address:

<code>2001:4898:9:3:c069:aa97:fe76:2449
</code>

an example for a share might be the following:

<code>\\2001-4898-9-3-c069-aa97-fe76-2449.ipv6-literal.net\share</code>

Other network providers may support the <b>lpRemoteName</b> member of the <a href="ns-winnetwk-netresourcea.md">NETRESOURCE</a> structure pointed to by the <i>lpNetResource</i> parameter that contains an IPv4 or IPv6 address, but this is up to specific network provider.

<b>Windows 7 and Windows Server 2008 R2:  </b>If the <b>WNetAddConnection3</b> function is called with explicit user credentials specified in the <i>pUsername</i> and <i>lpPassword</i> to establish a connection with a network resource on a specific server and then called again with either of these parameters as <b>NULL</b> (to use the default user name or default password) to the same server, the call with fail. The error returned will be <b>ERROR_BAD_USERNAME</b> or <b>ERROR_INVALID_PASSWORD</b>. 





> [!NOTE]
> The winnetwk.h header defines WNetAddConnection3 as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="ns-winnetwk-netresourcea.md">NETRESOURCE</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a">WNetAddConnection2</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnection2a">WNetCancelConnection2</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetconnectiona">WNetGetConnection</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetuseconnectiona">WNetUseConnection</a>



<a href="/windows/desktop/WNet/windows-networking-wnet-">Windows
		  Networking (WNet) Overview</a>



<a href="/windows/desktop/WNet/windows-networking-functions">Windows
		  Networking Functions</a>
