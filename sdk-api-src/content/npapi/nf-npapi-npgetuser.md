---
UID: NF:npapi.NPGetUser
title: NPGetUser function (npapi.h)
description: Retrieves the value of the current default user name or the user name used to establish a network connection.
helpviewer_keywords: ["NPGetUser","NPGetUser function [Security]","_mnp_npgetuser","npapi/NPGetUser","security.npgetuser"]
old-location: security\npgetuser.htm
tech.root: security
ms.assetid: 15fdf8fa-417c-4c1e-803e-6345cb4216e0
ms.date: 12/05/2018
ms.keywords: NPGetUser, NPGetUser function [Security], _mnp_npgetuser, npapi/NPGetUser, security.npgetuser
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
 - NPGetUser
 - npapi/NPGetUser
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
 - NPGetUser
---

# NPGetUser function


## -description

Retrieves the value of the current default user name or the user name used to establish a network connection.

## -parameters

### -param lpName [in]

Pointer to the name of the local device the caller is interested in, or a remote name for a resource that the user has made a connection to. This parameter may be <b>NULL</b> or the empty string if the caller is interested in the name of the user currently logged on to the system. If a remote name for a resource is passed in, and the user is connected to that resource using different names, it is possible that a provider cannot resolve which user name to return. In this case the provider may make an arbitrary choice amongst the possible user names.

### -param lpUserName [out]

Pointer to a buffer to receive the user name. This should be a name that can be passed into the 
<a href="/windows/desktop/api/npapi/nf-npapi-npaddconnection">NPAddConnection</a> or 
<a href="/windows/desktop/api/npapi/nf-npapi-npaddconnection3">NPAddConnection3</a> function to re-establish the connection with the same user name.

### -param lpnBufferLen [in, out]

Pointer to the size, in characters, of the <i>lpUserName</i> buffer. If the call fails because the buffer is not big enough, this location will be used to return the required buffer size.

## -returns

If the function succeeds, it should return WN_SUCCESS. Otherwise it should return an error code, which can be one of the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The value in the <i>lpName</i> parameter is not the name of a redirected device or a connected remote name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The buffer, <i>lpUserName</i>, is too small.

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