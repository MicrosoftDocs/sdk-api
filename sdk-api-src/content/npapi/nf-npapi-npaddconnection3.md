---
UID: NF:npapi.NPAddConnection3
title: NPAddConnection3 function (npapi.h)
description: Connects a local device to a network resource. (NPAddConnection3)
helpviewer_keywords: ["CONNECT_DEFERRED","CONNECT_INTERACTIVE","CONNECT_PROMPT","CONNECT_TEMPORARY","NPAddConnection3","NPAddConnection3 function [Security]","_mnp_npaddconnection3","dwType","lpLocalName","lpRemoteName","npapi/NPAddConnection3","security.npaddconnection3"]
old-location: security\npaddconnection3.htm
tech.root: security
ms.assetid: b0d730f7-595e-4ea7-8688-db479dcc40b4
ms.date: 12/05/2018
ms.keywords: CONNECT_DEFERRED, CONNECT_INTERACTIVE, CONNECT_PROMPT, CONNECT_TEMPORARY, NPAddConnection3, NPAddConnection3 function [Security], _mnp_npaddconnection3, dwType, lpLocalName, lpRemoteName, npapi/NPAddConnection3, security.npaddconnection3
req.header: npapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: davclnt.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NPAddConnection3
 - npapi/NPAddConnection3
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Npapi.h
api_name:
 - NPAddConnection3
---

# NPAddConnection3 function


## -description

The <b>NPAddConnection3</b> function connects a local device to a network resource. It performs the same operation as 
<a href="/windows/desktop/api/npapi/nf-npapi-npaddconnection">NPAddConnection</a> but in addition lets you specify a handle to the window that should own any resulting dialog boxes and specify how the connection should be established.

## -parameters

### -param hwndOwner [in]

A handle to a window that should own any messages or dialog boxes. This handle is valid only if CONNECT_INTERACTIVE is set in <i>dwFlags</i>, and the handle should only be used to produce dialog boxes needed for authentication.

### -param lpNetResource [in]

Pointer to a 
<a href="/windows/desktop/api/winnetwk/ns-winnetwk-netresourcea">NETRESOURCE</a> structure that specifies the network resource to connect to. The following fields must be set when making a connection. The others are ignored.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="lpRemoteName"></a><a id="lpremotename"></a><a id="LPREMOTENAME"></a><dl>
<dt><b>lpRemoteName</b></dt>
</dl>
</td>
<td width="60%">
Specifies the network resource to connect to.

</td>
</tr>
<tr>
<td width="40%"><a id="lpLocalName"></a><a id="lplocalname"></a><a id="LPLOCALNAME"></a><dl>
<dt><b>lpLocalName</b></dt>
</dl>
</td>
<td width="60%">
Specifies the name of a local device to be redirected, such as "F:" or "LPT1". This name is treated as case insensitive and may be the empty string or <b>NULL</b> pointer. If the string is empty or <b>NULL</b>, the function connects to the network resource without making a redirection.

</td>
</tr>
<tr>
<td width="40%"><a id="dwType"></a><a id="dwtype"></a><a id="DWTYPE"></a><dl>
<dt><b>dwType</b></dt>
</dl>
</td>
<td width="60%">
Specifies the type of resource to connect to. This can be RESOURCETYPE_DISK, RESOURCETYPE_PRINT, or RESOURCETYPE_ANY. The value RESOURCETYPE_ANY is used if the caller does not care or does not know.

</td>
</tr>
</table>

### -param lpPassword [in]

Pointer to the password to be used in making the connection, normally the password associated with <i>lpUserName</i>. The <b>NULL</b> value may be passed in to cause the function to use the default password. An empty string may be used to indicate no password. When you have finished using the password, clear it from memory by calling the <a href="/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a> function. For more information about protecting the password, see <a href="/windows/desktop/SecBP/handling-passwords">Handling Passwords</a>.

### -param lpUserName [in]

Pointer to the user name used to make the connection. If <b>NULL</b>, the default user name (that of the currently logged-on user) is applied. This is used when the user wants to connect to a resource but has a different assigned user name or account for that resource.

### -param dwFlags [in]

Any combination of the following values. The provider should ignore any other bits of <i>dwFlags</i> that may be set.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CONNECT_TEMPORARY"></a><a id="connect_temporary"></a><dl>
<dt><b>CONNECT_TEMPORARY</b></dt>
</dl>
</td>
<td width="60%">
The connection is being established for browsing purposes and will probably be released quickly.

</td>
</tr>
<tr>
<td width="40%"><a id="CONNECT_INTERACTIVE"></a><a id="connect_interactive"></a><dl>
<dt><b>CONNECT_INTERACTIVE</b></dt>
</dl>
</td>
<td width="60%">
The connection may have interaction with the user for authentication purposes.

</td>
</tr>
<tr>
<td width="40%"><a id="CONNECT_PROMPT"></a><a id="connect_prompt"></a><dl>
<dt><b>CONNECT_PROMPT</b></dt>
</dl>
</td>
<td width="60%">
Do not use any defaults for user names or passwords without offering the user a chance to supply an alternative. This flag is only valid if CONNECT_INTERACTIVE is also set.

</td>
</tr>
<tr>
<td width="40%"><a id="CONNECT_DEFERRED"></a><a id="connect_deferred"></a><dl>
<dt><b>CONNECT_DEFERRED</b></dt>
</dl>
</td>
<td width="60%">
Do not perform any remote network operations to make the network connection; instead, restore the connection in a "disconnected state." Attempt the actual connection only when some process attempts to use the connection. If this bit is set, the caller must supply <i>lpLocalName</i>. 




This feature is used to speed the restoring of network connections at logon. A provider that supports it should return the WNNC_CON_DEFERRED bit in <a href="/windows/desktop/api/npapi/nf-npapi-npgetcaps">NPGetCaps</a>.

</td>
</tr>
</table>

## -returns

If the function succeeds, it will return WN_SUCCESS. Otherwise, it will return an error code. This may include one of the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_BAD_NETNAME</b></dt>
</dl>
</td>
<td width="60%">
The value of the <b>lpRemoteName</b> member of the structure passed into <i>lpNetResource</i> is not valid for this provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_BAD_LOCALNAME</b></dt>
</dl>
</td>
<td width="60%">
The value of the <b>lpLocalName</b> member of the structure passed into <i>lpNetResource</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_BAD_PASSWORD</b></dt>
</dl>
</td>
<td width="60%">
The specified password is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_ALREADY_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The device specified in the <b>lpLocalName</b> member of the structure passed into <i>lpNetResource</i> is already connected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Permission to establish the connection is denied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_NO_NETWORK</b></dt>
</dl>
</td>
<td width="60%">
The network is not present.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_CANCEL</b></dt>
</dl>
</td>
<td width="60%">
The attempt to make the connection was canceled by the user using a dialog box displayed by the provider.

</td>
</tr>
</table>

## -remarks

If a provider displays a password dialog box because the specified credentials are insufficient and the CONNECT_INTERACTIVE flag is set, then the provider may not return an access-denied error code (one of ERROR_LOGON_FAILURE, WN_BAD_PASSWORD, WN_ACCESS_DENIED). The suggested behavior is for the provider to continue asking the user for valid credentials until the user either supplies them or presses a "cancel" button. If <b>NPAddConnection3</b> is called to make the connection requested during the 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetconnectiondialog">WNetConnectionDialog</a> or 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetconnectiondialog1a">WNetConnectionDialog1</a> function and an access-denied code is returned, the 
<b>WNetConnectionDialog</b> or 
<b>WNetConnectionDialog1</b> function will, itself, display a password dialog box.

## -see-also

<a href="/windows/desktop/api/npapi/nf-npapi-npaddconnection">NPAddConnection</a>
