---
UID: NF:npapi.NPAddConnection
title: NPAddConnection function (npapi.h)
description: Connects a local device to a network resource. (NPAddConnection)
helpviewer_keywords: ["NPAddConnection","NPAddConnection function [Security]","_mnp_npaddconnection","dwType","lpLocalName","lpRemoteName","npapi/NPAddConnection","security.npaddconnection"]
old-location: security\npaddconnection.htm
tech.root: security
ms.assetid: 37a3988c-18ee-400a-85c3-cc3cbdf015ea
ms.date: 12/05/2018
ms.keywords: NPAddConnection, NPAddConnection function [Security], _mnp_npaddconnection, dwType, lpLocalName, lpRemoteName, npapi/NPAddConnection, security.npaddconnection
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
 - NPAddConnection
 - npapi/NPAddConnection
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
 - NPAddConnection
---

# NPAddConnection function


## -description

The <b>NPAddConnection</b> function connects a local device to a network resource.

## -parameters

### -param lpNetResource [in]

Pointer to a 
<a href="/windows/desktop/api/winnetwk/ns-winnetwk-netresourcea">NETRESOURCE</a> structure which specifies the network resource to connect to. The following fields must be set in the <b>NETRESOURCE</b> structure you pass in. The <b>NPAddConnection</b> function ignores the other fields.

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
Specifies the name of a local device to be redirected, such as "F:" or "LPT1". This name is treated as case insensitive and may be an empty string or <b>NULL</b> pointer. If the string is empty or <b>NULL</b>, the function connects to the network resource without making a redirection.

</td>
</tr>
<tr>
<td width="40%"><a id="dwType"></a><a id="dwtype"></a><a id="DWTYPE"></a><dl>
<dt><b>dwType</b></dt>
</dl>
</td>
<td width="60%">
Specifies the type of resource to connect to. This can be RESOURCETYPE_DISK, RESOURCETYPE _PRINT, or RESOURCETYPE_ANY. The value RESOURCETYPE _ANY is used if the caller does not care or does not know.

</td>
</tr>
</table>

### -param lpPassword [in]

Pointer to the password to be used in making the connection, normally the password associated with <i>lpUserName</i>. The <b>NULL</b> value may be passed in to cause the function to use the default password. An empty string may be used to indicate no password. When you have finished using the password, clear it from memory by calling the <a href="/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a> function. For more information about protecting the password, see <a href="/windows/desktop/SecBP/handling-passwords">Handling Passwords</a>.

### -param lpUserName [in]

Pointer to the user name used to make the connection. If <b>NULL</b>, the default user name (that of the currently logged-on user) is applied. This is used when the user wants to connect to a resource but has a different assigned user name or account for that resource.

For example, if you were logged using the user name "MyAccount" and wanted to connect to a network resource that was available only to a second account, where the user name was "MyOtherAccount", you could specify "MyOtherAccount" in <i>lpUserName</i> in order to connect to the resource. You would also specify the password of this second account in <i>lpPassword</i>.

## -returns

If the function succeeds, it should return WN_SUCCESS. Otherwise, it should return an error code, which can be one of the following.

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
</table>
