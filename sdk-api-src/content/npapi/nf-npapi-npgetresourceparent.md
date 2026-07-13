---
UID: NF:npapi.NPGetResourceParent
title: NPGetResourceParent function (npapi.h)
description: Retrieves the parent of a specified network resource in the browse hierarchy.
helpviewer_keywords: ["NPGetResourceParent","NPGetResourceParent function [Security]","_mnp_npgetresourceparent","npapi/NPGetResourceParent","security.npgetresourceparent"]
old-location: security\npgetresourceparent.htm
tech.root: security
ms.assetid: 48add326-7182-426a-b7b6-d56f4bfcfb2b
ms.date: 12/05/2018
ms.keywords: NPGetResourceParent, NPGetResourceParent function [Security], _mnp_npgetresourceparent, npapi/NPGetResourceParent, security.npgetresourceparent
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
 - NPGetResourceParent
 - npapi/NPGetResourceParent
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
 - NPGetResourceParent
---

# NPGetResourceParent function


## -description

Retrieves the parent of a specified network resource in the browse hierarchy. This function is typically called for resources that were returned by the same provider from prior calls to 
<a href="/windows/desktop/api/npapi/nf-npapi-npenumresource">NPEnumResource</a> or 
<a href="/windows/desktop/api/npapi/nf-npapi-npgetresourceinformation">NPGetResourceInformation</a>.

## -parameters

### -param lpNetResource [in]

Pointer to the network resource whose parent name is required. The 
<a href="/windows/desktop/api/winnetwk/ns-winnetwk-netresourcea">NETRESOURCE</a> could have been obtained from a previous call to 
<a href="/windows/desktop/api/npapi/nf-npapi-npenumresource">NPEnumResource</a> or 
<a href="/windows/desktop/api/npapi/nf-npapi-npgetresourceinformation">NPGetResourceInformation</a>, or constructed by the caller. 




The <b>lpRemoteName</b> field specifies the remote name of the network resource whose parent is required.

The <b>lpProvider</b> field specifies the provider to call. This must be supplied.

The <b>dwType</b> field is filled in if the calling program knows its value. Otherwise, it is set to <b>NULL</b>.

All other fields in the <a href="/windows/desktop/api/winnetwk/ns-winnetwk-netresourcea">NETRESOURCE</a> are ignored and are not initialized.

### -param lpBuffer [out]

Pointer to a buffer to receive the result, which is a single <a href="/windows/desktop/api/winnetwk/ns-winnetwk-netresourcea">NETRESOURCE</a> structure representing the parent resource. The <b>lpRemoteName</b>, <b>lpProvider</b>, <b>dwType</b>, <b>dwDisplayType</b>, and <b>dwUsage</b> fields are returned; all other fields are set to <b>NULL</b>. 




The output <b>lpRemoteName</b> should be in the same format as that returned from an enumeration by 
<a href="/windows/desktop/api/npapi/nf-npapi-npenumresource">NPEnumResource</a>, so that the caller can perform a case-sensitive string comparison to determine whether the parent resource is the same as one returned by <b>NPEnumResource</b>. If the input resource syntactically has a parent, the provider can return it, without determining whether the input resource or its parent actually exist. If a resource has no browse parent on the network, then <b>lpRemoteName</b> is returned as <b>NULL</b>.

The RESOURCEUSAGE_CONNECTABLE bit in the returned <b>dwUsage</b> field does not necessarily indicate that the resource can currently be connected to, only that the resource is connectable when it is available on the network.

### -param lpBufferSize [in, out]

Pointer to a location that specifies the size, in bytes, of the buffer pointed to by the <i>lpBuffer</i> parameter. If the buffer is too small for the result, the function places the required buffer size at this location and returns the error WN_MORE_DATA.

## -returns

If the function succeeds, it should return WN_SUCCESS. Otherwise, it should return an error code, which may be one of the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The input buffer is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_BAD_NETNAME</b></dt>
</dl>
</td>
<td width="60%">
This provider does not own the resource specified by <i>lpNetResource</i> (or the resource is syntactically not valid).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_BAD_VALUE</b></dt>
</dl>
</td>
<td width="60%">
Either <b>dwUsage</b> or <b>dwType</b> is not valid, or there is an incorrect combination of parameters specified (for example, <b>lpRemoteName</b> is syntactically not valid for <b>dwType</b>).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_NOT_AUTHENTICATED</b></dt>
</dl>
</td>
<td width="60%">
The caller has not been authenticated to the network.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller has been authenticated to the network, but does not have sufficient permissions.

</td>
</tr>
</table>