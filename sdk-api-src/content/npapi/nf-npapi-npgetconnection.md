---
UID: NF:npapi.NPGetConnection
title: NPGetConnection function (npapi.h)
description: Retrieves information about a connection.
helpviewer_keywords: ["NPGetConnection","NPGetConnection function [Security]","_mnp_npgetconnection","npapi/NPGetConnection","security.npgetconnection"]
old-location: security\npgetconnection.htm
tech.root: security
ms.assetid: 3f52bbff-998d-4e11-877f-478085207e6b
ms.date: 12/05/2018
ms.keywords: NPGetConnection, NPGetConnection function [Security], _mnp_npgetconnection, npapi/NPGetConnection, security.npgetconnection
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
 - NPGetConnection
 - npapi/NPGetConnection
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
 - NPGetConnection
---

# NPGetConnection function


## -description

Retrieves information about a connection.

## -parameters

### -param lpLocalName [in]

Pointer to the name of the local device the caller is interested in. The network provider can assume this name is syntactically valid.

### -param lpRemoteName [out]

Pointer to a buffer that will receive the remote name used to make the connection. This buffer is allocated by the caller.

### -param lpnBufferLen [in, out]

Pointer to the size, in characters, of the <i>lpRemoteName</i> buffer. If the call fails because the buffer is not big enough, <i>lpBufferSize</i> is set to the required buffer size.

## -returns

If the function succeeds, it should return WN_SUCCESS. Otherwise, it should return an error code, which can be one of the following:

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
The device specified by <i>lpLocalName</i> is not redirected by this provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The buffer was too small to receive all of the data.

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

## -remarks

The <b>NPGetConnection</b> function can return information only about a network connection that is currently connected. To retrieve information about a network connection that is currently disconnected, use 
<a href="/windows/desktop/api/npapi/nf-npapi-npgetconnection3">NPGetConnection3</a>.