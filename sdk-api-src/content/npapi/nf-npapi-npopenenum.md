---
UID: NF:npapi.NPOpenEnum
title: NPOpenEnum function (npapi.h)
description: Opens an enumeration of network resources or existing connections. The NPOpenEnum function must be called to obtain a valid handle for an enumeration.
helpviewer_keywords: ["NPOpenEnum","NPOpenEnum function [Security]","RESOURCETYPE_DISK","RESOURCETYPE_PRINT","RESOURCEUSAGE_ATTACHED","RESOURCEUSAGE_CONNECTABLE","RESOURCEUSAGE_CONTAINER","RESOURCE_CONNECTED","RESOURCE_CONTEXT","RESOURCE_GLOBALNET","_mnp_npopenenum","npapi/NPOpenEnum","security.npopenenum"]
old-location: security\npopenenum.htm
tech.root: security
ms.assetid: d8fa7336-3ede-4445-b2e8-1a3efcae22ff
ms.date: 12/05/2018
ms.keywords: NPOpenEnum, NPOpenEnum function [Security], RESOURCETYPE_DISK, RESOURCETYPE_PRINT, RESOURCEUSAGE_ATTACHED, RESOURCEUSAGE_CONNECTABLE, RESOURCEUSAGE_CONTAINER, RESOURCE_CONNECTED, RESOURCE_CONTEXT, RESOURCE_GLOBALNET, _mnp_npopenenum, npapi/NPOpenEnum, security.npopenenum
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
 - NPOpenEnum
 - npapi/NPOpenEnum
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
 - NPOpenEnum
---

# NPOpenEnum function


## -description

Opens an enumeration of network resources or existing connections. The <b>NPOpenEnum</b> function must be called to obtain a valid handle for an enumeration.

## -parameters

### -param dwScope [in]

Determines the scope of the enumeration. This can be one of the following. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RESOURCE_CONNECTED"></a><a id="resource_connected"></a><dl>
<dt><b>RESOURCE_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
All currently connected resources.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCE_GLOBALNET"></a><a id="resource_globalnet"></a><dl>
<dt><b>RESOURCE_GLOBALNET</b></dt>
</dl>
</td>
<td width="60%">
All resources on the network.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCE_CONTEXT"></a><a id="resource_context"></a><dl>
<dt><b>RESOURCE_CONTEXT</b></dt>
</dl>
</td>
<td width="60%">
The resources associated with the user's current and default network context (used for a "Network Neighborhood" view). The interpretation of this is left to the provider.

</td>
</tr>
</table>

### -param dwType [in]

Specifies the type of resources of interest. This is a bitmask, which may be any combination of the following flags. 





<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RESOURCETYPE_DISK"></a><a id="resourcetype_disk"></a><dl>
<dt><b>RESOURCETYPE_DISK</b></dt>
</dl>
</td>
<td width="60%">
All disk resources.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCETYPE_PRINT"></a><a id="resourcetype_print"></a><dl>
<dt><b>RESOURCETYPE_PRINT</b></dt>
</dl>
</td>
<td width="60%">
All print resources.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCEUSAGE_ATTACHED"></a><a id="resourceusage_attached"></a><dl>
<dt><b>RESOURCEUSAGE_ATTACHED</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the function should fail if the caller is not authenticated (even if the network permits enumeration without authentication).

</td>
</tr>
</table>
 

If <i>dwType</i> is 0, or is just RESOURCEUSAGE_ATTACHED, all types of resources are returned. If a provider does not have the capability to distinguish between print and disk resources at the same level, it may return all resources.

### -param dwUsage [in]

Specifies the usage of resources of interested. This is a bitmask, which may be any combination of the following flags. 





<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RESOURCEUSAGE_CONNECTABLE"></a><a id="resourceusage_connectable"></a><dl>
<dt><b>RESOURCEUSAGE_CONNECTABLE</b></dt>
</dl>
</td>
<td width="60%">
All connectable resources

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCEUSAGE_CONTAINER"></a><a id="resourceusage_container"></a><dl>
<dt><b>RESOURCEUSAGE_CONTAINER</b></dt>
</dl>
</td>
<td width="60%">
All container resources

</td>
</tr>
</table>
 

The bitmask may be zero to match all of the flags. This parameter may be ignored if <i>dwScope</i> is not set to RESOURCE_GLOBALNET.

### -param lpNetResource [in]

Pointer to the container to perform the enumeration. The 
<a href="/windows/desktop/api/winnetwk/ns-winnetwk-netresourcea">NETRESOURCE</a> could have been obtained through a previous <a href="/windows/desktop/api/npapi/nf-npapi-npenumresource">NPEnumResource</a> call, or constructed by the caller, or it can be <b>NULL</b>. If it is <b>NULL</b> or if the <b>lpRemoteName</b> field of the <b>NETRESOURCE</b> is <b>NULL</b>, the provider should enumerate the top level of its network. Note that this means a provider cannot use an <b>lpRemoteName</b> of <b>NULL</b> to represent any network resource. A caller would normally start off by calling <b>NPOpenEnum</b> with this parameter set to <b>NULL</b> and then use the returned results for further enumeration. If the calling program knows exactly the provider and remote path to enumerate from, it may build its own <b>NETRESOURCE</b> structure to pass in, filling in the <b>lpProvider</b> and <b>lpRemoteName</b> fields. Note that if <i>dwScope</i> is RESOURCE_CONNECTED or RESOURCE_CONTEXT, this parameter will be <b>NULL</b>.

### -param lphEnum [out]

Pointer to a handle that can be used by the <a href="/windows/desktop/api/npapi/nf-npapi-npenumresource">NPEnumResource</a> function. When you have finished using the handle, release the handle by calling the <a href="/windows/desktop/api/npapi/nf-npapi-npcloseenum">NPCloseEnum</a> function.

## -returns

If the function succeeds, it should return WN_SUCCESS. Otherwise, it should return an error code which may include one of the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The provider does not support the type of enumeration being requested, or the specific network resource cannot be browsed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_NOT_CONTAINER</b></dt>
</dl>
</td>
<td width="60%">
<i>lpNetResource</i> does not point to a container.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_BAD_VALUE</b></dt>
</dl>
</td>
<td width="60%">
Invalid <i>dwScope</i>, <i>dwUsage</i>, or <i>dwType</i> or bad combination of parameters is specified.

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