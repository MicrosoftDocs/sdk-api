---
UID: NS:winnetwk._NETRESOURCEW
title: NETRESOURCEW (winnetwk.h)
description: The following structure contains information about a network resource. It is used by several of the network provider functions, including NPOpenEnum and NPAddConnection. (Unicode)
helpviewer_keywords: ["*LPNETRESOURCEW","LPNETRESOURCE","LPNETRESOURCE structure pointer [Security]","NETRESOURCE","NETRESOURCE structure [Security]","NETRESOURCEA","NETRESOURCEW","RESOURCEDISPLAYTYPE_DIRECTORY","RESOURCEDISPLAYTYPE_DOMAIN","RESOURCEDISPLAYTYPE_GENERIC","RESOURCEDISPLAYTYPE_NETWORK","RESOURCEDISPLAYTYPE_SERVER","RESOURCEDISPLAYTYPE_SHARE","RESOURCETYPE_ANY","RESOURCETYPE_DISK","RESOURCETYPE_PRINT","RESOURCEUSAGE_CONNECTABLE","RESOURCEUSAGE_CONTAINER","RESOURCE_CONNECTED","RESOURCE_CONTEXT","RESOURCE_GLOBALNET","_mnp_netresource","security.netresource","winnetwk/LPNETRESOURCE","winnetwk/NETRESOURCE","winnetwk/NETRESOURCEA","winnetwk/NETRESOURCEW"]
old-location: security\netresource.htm
tech.root: security
ms.assetid: c7e22694-2dfd-4a9e-bd40-277611476f97
ms.date: 12/05/2018
ms.keywords: '*LPNETRESOURCEW, LPNETRESOURCE, LPNETRESOURCE structure pointer [Security], NETRESOURCE, NETRESOURCE structure [Security], NETRESOURCEA, NETRESOURCEW, RESOURCEDISPLAYTYPE_DIRECTORY, RESOURCEDISPLAYTYPE_DOMAIN, RESOURCEDISPLAYTYPE_GENERIC, RESOURCEDISPLAYTYPE_NETWORK, RESOURCEDISPLAYTYPE_SERVER, RESOURCEDISPLAYTYPE_SHARE, RESOURCETYPE_ANY, RESOURCETYPE_DISK, RESOURCETYPE_PRINT, RESOURCEUSAGE_CONNECTABLE, RESOURCEUSAGE_CONTAINER, RESOURCE_CONNECTED, RESOURCE_CONTEXT, RESOURCE_GLOBALNET, _mnp_netresource, security.netresource, winnetwk/LPNETRESOURCE, winnetwk/NETRESOURCE, winnetwk/NETRESOURCEA, winnetwk/NETRESOURCEW'
req.header: winnetwk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: NETRESOURCEW (Unicode) and NETRESOURCEA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NETRESOURCEW, *LPNETRESOURCEW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NETRESOURCEW
 - winnetwk/_NETRESOURCEW
 - LPNETRESOURCEW
 - winnetwk/LPNETRESOURCEW
 - NETRESOURCEW
 - winnetwk/NETRESOURCEW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnetwk.h
api_name:
 - NETRESOURCE
 - NETRESOURCEA
 - NETRESOURCEW
---

# NETRESOURCEW structure


## -description

The following structure contains information about a network resource. It is used by several of the network provider functions, including 
<a href="/windows/desktop/api/npapi/nf-npapi-npopenenum">NPOpenEnum</a> 
and <a href="/windows/desktop/api/npapi/nf-npapi-npaddconnection">NPAddConnection</a>.

## -struct-fields

### -field dwScope

Indicates the scope of the enumeration. This can be one of the following values.

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
Current connections to network resources.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCE_GLOBALNET"></a><a id="resource_globalnet"></a><dl>
<dt><b>RESOURCE_GLOBALNET</b></dt>
</dl>
</td>
<td width="60%">
All network resources. These may or may not be connected.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCE_CONTEXT"></a><a id="resource_context"></a><dl>
<dt><b>RESOURCE_CONTEXT</b></dt>
</dl>
</td>
<td width="60%">
The network resources associated with the user's current and default network context. The meaning of this is provider-specific.

</td>
</tr>
</table>

### -field dwType

Indicates the resource type. This can be one of the following values.

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
The resource is a shared disk volume.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCETYPE_PRINT"></a><a id="resourcetype_print"></a><dl>
<dt><b>RESOURCETYPE_PRINT</b></dt>
</dl>
</td>
<td width="60%">
The resource is a shared printer.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCETYPE_ANY"></a><a id="resourcetype_any"></a><dl>
<dt><b>RESOURCETYPE_ANY</b></dt>
</dl>
</td>
<td width="60%">
The resource matches more than one type, for example, a container of both print and disk resources, or a resource which is neither print or disk.

</td>
</tr>
</table>

### -field dwDisplayType

Set by the provider to indicate what display type a user interface should use to represent this resource. The following types are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RESOURCEDISPLAYTYPE_NETWORK"></a><a id="resourcedisplaytype_network"></a><dl>
<dt><b>RESOURCEDISPLAYTYPE_NETWORK</b></dt>
</dl>
</td>
<td width="60%">
The resource is a network provider.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCEDISPLAYTYPE_DOMAIN"></a><a id="resourcedisplaytype_domain"></a><dl>
<dt><b>RESOURCEDISPLAYTYPE_DOMAIN</b></dt>
</dl>
</td>
<td width="60%">
The resource is a collection of servers.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCEDISPLAYTYPE_SERVER"></a><a id="resourcedisplaytype_server"></a><dl>
<dt><b>RESOURCEDISPLAYTYPE_SERVER</b></dt>
</dl>
</td>
<td width="60%">
The resource is a server.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCEDISPLAYTYPE_SHARE"></a><a id="resourcedisplaytype_share"></a><dl>
<dt><b>RESOURCEDISPLAYTYPE_SHARE</b></dt>
</dl>
</td>
<td width="60%">
The resource is a share point.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCEDISPLAYTYPE_DIRECTORY"></a><a id="resourcedisplaytype_directory"></a><dl>
<dt><b>RESOURCEDISPLAYTYPE_DIRECTORY</b></dt>
</dl>
</td>
<td width="60%">
The resource is a directory.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCEDISPLAYTYPE_GENERIC"></a><a id="resourcedisplaytype_generic"></a><dl>
<dt><b>RESOURCEDISPLAYTYPE_GENERIC</b></dt>
</dl>
</td>
<td width="60%">
The resource type is unspecified. This value is used by network providers that do not specify resource types.

</td>
</tr>
</table>

### -field dwUsage

A bitmask that indicates how you can enumerate information about the resource. It is defined only if <b>dwScope</b> is set to RESOURCE_GLOBALNET. The <b>dwUsage</b> field can contain one or more of the following flags.

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
You can connect to the resource by calling 
<a href="/windows/desktop/api/npapi/nf-npapi-npaddconnection">NPAddConnection</a>. If <b>dwType</b> is RESOURCETYPE_DISK, then, after you have connected to the resource, you can use the file system APIs, such as 
<a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfilew">FindFirstFile</a>, and 
<a href="/windows/desktop/api/fileapi/nf-fileapi-findnextfilew">FindNextFile</a>, to enumerate any files and directories the resource contains.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCEUSAGE_CONTAINER"></a><a id="resourceusage_container"></a><dl>
<dt><b>RESOURCEUSAGE_CONTAINER</b></dt>
</dl>
</td>
<td width="60%">
The resource is a container for other resources that can be enumerated by means of the 
<a href="/windows/desktop/api/npapi/nf-npapi-npopenenum">NPOpenEnum</a>, 
<a href="/windows/desktop/api/npapi/nf-npapi-npenumresource">NPEnumResource</a>, and 
<a href="/windows/desktop/api/npapi/nf-npapi-npcloseenum">NPCloseEnum</a> functions. 




The container may, however, be empty at the time  the enumeration is made. In other words, the first call to <a href="/windows/desktop/api/npapi/nf-npapi-npenumresource">NPEnumResource</a> may return WN_NO_MORE_ENTRIES.

</td>
</tr>
</table>

### -field lpLocalName

If <b>dwScope</b> is RESOURCE_CONNECTED, the <b>lpLocalName</b> field contains the name of a redirected device. If the connection is a deviceless connection, this field contains <b>NULL</b>. 




If <b>dwScope</b> is not set to RESOURCE_CONNECTED, this field is undefined.

### -field lpRemoteName

If the enumerated item is a network resource, this field contains a remote network name. This name may be then passed to 
<a href="/windows/desktop/api/npapi/nf-npapi-npaddconnection">NPAddConnection</a> to make a network connection if <b>dwUsage</b> is set to RESOURCEUSAGE_CONNECTABLE. If the enumerated item is a current connection, this field will refer to the remote network name that <b>lpLocalName</b> is connected to.

### -field lpComment

May be any provider-supplied comment associated with the enumerated item.

### -field lpProvider

Specifies the name of the provider that owns this enumerated item.

## -remarks

> [!NOTE]
> The winnetwk.h header defines NETRESOURCE as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
