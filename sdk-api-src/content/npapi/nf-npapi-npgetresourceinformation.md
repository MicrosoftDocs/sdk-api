---
UID: NF:npapi.NPGetResourceInformation
title: NPGetResourceInformation function (npapi.h)
description: Separates the part of a network resource accessed through the WNet API from the part accessed through APIs specific to the resource type.
helpviewer_keywords: ["NPGetResourceInformation","NPGetResourceInformation function [Security]","_mnp_npgetresourceinformation","npapi/NPGetResourceInformation","security.npgetresourceinformation"]
old-location: security\npgetresourceinformation.htm
tech.root: security
ms.assetid: c256dec0-6e5c-4a67-bc99-c322086a8fc7
ms.date: 12/05/2018
ms.keywords: NPGetResourceInformation, NPGetResourceInformation function [Security], _mnp_npgetresourceinformation, npapi/NPGetResourceInformation, security.npgetresourceinformation
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
 - NPGetResourceInformation
 - npapi/NPGetResourceInformation
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
 - NPGetResourceInformation
---

# NPGetResourceInformation function


## -description

Separates the part of a network resource accessed through the WNet API from the part accessed through APIs specific to the resource type.

## -parameters

### -param lpNetResource [in]

Specifies the network resource for which information is required. The <b>lpRemoteName</b> field specifies the remote name of the resource. The calling program should fill in the values for the <b>lpProvider</b> and <b>dwType</b> fields if it knows these values; otherwise, it should set these fields to <b>NULL</b>. All other fields in the <a href="/windows/desktop/api/winnetwk/ns-winnetwk-netresourcea">NETRESOURCE</a> are ignored and are not initialized. 




If the <b>lpRemoteName</b> string contains a portion that is accessed through WNet APIs and a portion that is accessed through other system APIs specific to the resource type, the function should return information only about the network portion of the resource (except for <i>lplpSystem</i>, as described later in this topic).

For example, if the resource is "\\server\share\dir1\dir2", where "\\server\share" is accessed through WNet APIs and "\dir1\dir2" is accessed through file system APIs, the provider should verify that it is the right provider for "\\server\share", but need not check whether "\dir1\dir2" actually exists.

### -param lpBuffer [out]

Pointer to the buffer to receive the result. The first field in the result is a single 
<a href="/windows/desktop/api/winnetwk/ns-winnetwk-netresourcea">NETRESOURCE</a> structure, and associated strings, representing that portion of the input resource that is accessed through the WNet API, rather than system APIs specific to the resource type. For example, if the input remote resource name was "\\server\share\dir1\dir2", then the output <b>NETRESOURCE</b> contains information about the resource "\\server\share". The <b>lpRemoteName</b>, <b>lpProvider</b>, <b>dwType</b>, <b>dwDisplayType</b>, and <b>dwUsage</b> fields are returned containing values, all other fields being set to <b>NULL</b>. 




The <b>lpRemoteName</b> field should be returned in the same format as that returned from an enumeration by the 
<a href="/windows/desktop/api/npapi/nf-npapi-npenumresource">NPEnumResource</a> function, so that the caller can perform a case-sensitive string comparison. This is necessary to determine whether the output network resource is the same as one returned by <b>NPEnumResource</b>.

The provider should not do purely syntactic checking to determine whether it owns the resource. This could produce incorrect results when two networks are running on the client and the provider doing syntactic checking is called first.

### -param lpBufferSize [in, out]

Pointer to a location that specifies the size, in bytes, of the buffer pointed to by <i>lpBuffer</i>. If the buffer is too small for the result, the function places the required buffer size at this location and returns the error WN_MORE_DATA.

### -param lplpSystem [out]

On a successful return, a pointer to a <b>null</b>-terminated string in the output buffer specifying that part of the resource that is accessed through system APIs specific to the resource type, rather than through the WNet API. If there is no such part, <i>lplpSystem</i> is set to <b>NULL</b>. For example, if the input remote resource name was "\\server\share\dir", <b>lpRemoteName</b> is returned pointing to "\\server\share" and <i>lplpSystem</i> points to "\dir", both strings being stored in the buffer pointed to by <i>lpBuffer</i>.

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
The resource is not recognized by this provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_BAD_VALUE</b></dt>
</dl>
</td>
<td width="60%">
Invalid <i>dwUsage</i> or <i>dwType</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_BAD_DEV_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The caller passed in a nonzero <i>dwType</i> that does not match the actual type of the network resource.

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
The caller has been authenticated to the network but does not have sufficient permissions.

</td>
</tr>
</table>

## -remarks

The enumeration tree can be navigated down from a named network resource by using 
<a href="/windows/desktop/api/npapi/nf-npapi-npopenenum">NPOpenEnum</a> and its related functions. To navigate up from a named resource, the <b>NPGetResourceInformation</b> function can be called to obtain information about the resource, followed by the 
<a href="/windows/desktop/api/npapi/nf-npapi-npgetresourceparent">NPGetResourceParent</a> function to obtain the name and type of the parent resource.

<b>NPGetResourceInformation</b> determines whether the specified provider is the right provider to respond to a request for a specified network resource. It then returns information about the resource's type.