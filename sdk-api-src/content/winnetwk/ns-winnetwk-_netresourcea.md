---
UID: NS:winnetwk._NETRESOURCEA
title: "_NETRESOURCEA"
author: windows-sdk-content
description: Contains information about a network resource.
old-location: wnet\netresource_str.htm
tech.root: WNet
ms.assetid: c53d078e-188a-4371-bdb9-fc023bc0c1ba
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPNETRESOURCEA, NETRESOURCE, NETRESOURCE structure [Windows Networking (WNet)], NETRESOURCEA, RESOURCEDISPLAYTYPE_DIRECTORY, RESOURCEDISPLAYTYPE_DOMAIN, RESOURCEDISPLAYTYPE_FILE, RESOURCEDISPLAYTYPE_GENERIC, RESOURCEDISPLAYTYPE_GROUP, RESOURCEDISPLAYTYPE_NDSCONTAINER, RESOURCEDISPLAYTYPE_NETWORK, RESOURCEDISPLAYTYPE_ROOT, RESOURCEDISPLAYTYPE_SERVER, RESOURCEDISPLAYTYPE_SHARE, RESOURCEDISPLAYTYPE_SHAREADMIN, RESOURCEDISPLAYTYPE_TREE, RESOURCETYPE_ANY, RESOURCETYPE_DISK, RESOURCETYPE_PRINT, RESOURCEUSAGE_ATTACHED, RESOURCEUSAGE_CONNECTABLE, RESOURCEUSAGE_CONTAINER, RESOURCEUSAGE_NOLOCALDEVICE, RESOURCEUSAGE_SIBLING, RESOURCE_CONNECTED, RESOURCE_GLOBALNET, RESOURCE_REMEMBERED, _NETRESOURCEA, _NETRESOURCEW, _win32_netresource_str, winnetwk/NETRESOURCE, winnetwk/_NETRESOURCEA, winnetwk/_NETRESOURCEW, wnet.netresource_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winnetwk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: "_NETRESOURCEW (Unicode) and _NETRESOURCEA (ANSI)"
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnetwk.h
api_name:
 - NETRESOURCE
 - _NETRESOURCEA
 - _NETRESOURCEW
product: Windows
targetos: Windows
req.typenames: NETRESOURCEA, *LPNETRESOURCEA
req.redist: 
---

# _NETRESOURCEA structure


## -description


The
				<b>NETRESOURCE</b> structure contains information about a network resource.


## -struct-fields




### -field dwScope

Type: <b>DWORD</b>

The scope of the enumeration. This member can be one of the following values defined in the <i>Winnetwk.h</i> header file. 

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
Enumerate currently connected resources. The <b>dwUsage</b> member cannot be specified.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCE_GLOBALNET"></a><a id="resource_globalnet"></a><dl>
<dt><b>RESOURCE_GLOBALNET</b></dt>
</dl>
</td>
<td width="60%">
Enumerate all resources on the network. The <b>dwUsage</b> member is specified.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCE_REMEMBERED"></a><a id="resource_remembered"></a><dl>
<dt><b>RESOURCE_REMEMBERED</b></dt>
</dl>
</td>
<td width="60%">
Enumerate remembered (persistent) connections. The <b>dwUsage</b> member cannot be specified.

</td>
</tr>
</table>
 


### -field dwType

Type: <b>DWORD</b>

The type of resource. This member can be one of the following values defined in the <i>Winnetwk.h</i> header file.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RESOURCETYPE_ANY"></a><a id="resourcetype_any"></a><dl>
<dt><b>RESOURCETYPE_ANY</b></dt>
</dl>
</td>
<td width="60%">
All resources.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCETYPE_DISK"></a><a id="resourcetype_disk"></a><dl>
<dt><b>RESOURCETYPE_DISK</b></dt>
</dl>
</td>
<td width="60%">
Disk resources.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCETYPE_PRINT"></a><a id="resourcetype_print"></a><dl>
<dt><b>RESOURCETYPE_PRINT</b></dt>
</dl>
</td>
<td width="60%">
Print resources.

</td>
</tr>
</table>
 

The 
<a href="https://msdn.microsoft.com/2c58c6d0-d5fe-447e-be39-df34072c160e">WNetEnumResource</a> function can also return the value RESOURCETYPE_UNKNOWN if a resource is neither a disk nor a print resource.


### -field dwDisplayType

Type: <b>DWORD</b>

The display options for the network object  in a network browsing user interface. This member can be one of the following values defined in the <i>Winnetwk.h</i> header file. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RESOURCEDISPLAYTYPE_GENERIC"></a><a id="resourcedisplaytype_generic"></a><dl>
<dt><b>RESOURCEDISPLAYTYPE_GENERIC</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
The method used to display the object does not matter.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCEDISPLAYTYPE_DOMAIN"></a><a id="resourcedisplaytype_domain"></a><dl>
<dt><b>RESOURCEDISPLAYTYPE_DOMAIN</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The object should be displayed as a domain.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCEDISPLAYTYPE_SERVER"></a><a id="resourcedisplaytype_server"></a><dl>
<dt><b>RESOURCEDISPLAYTYPE_SERVER</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The object should be displayed as a server.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCEDISPLAYTYPE_SHARE"></a><a id="resourcedisplaytype_share"></a><dl>
<dt><b>RESOURCEDISPLAYTYPE_SHARE</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
The object should be displayed as a share.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCEDISPLAYTYPE_FILE"></a><a id="resourcedisplaytype_file"></a><dl>
<dt><b>RESOURCEDISPLAYTYPE_FILE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The object should be displayed as a file.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCEDISPLAYTYPE_GROUP"></a><a id="resourcedisplaytype_group"></a><dl>
<dt><b>RESOURCEDISPLAYTYPE_GROUP</b></dt>
<dt>0x00000005</dt>
</dl>
</td>
<td width="60%">
The object should be displayed as a group.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCEDISPLAYTYPE_NETWORK"></a><a id="resourcedisplaytype_network"></a><dl>
<dt><b>RESOURCEDISPLAYTYPE_NETWORK</b></dt>
<dt>0x00000006</dt>
</dl>
</td>
<td width="60%">
The object should be displayed as a network.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCEDISPLAYTYPE_ROOT"></a><a id="resourcedisplaytype_root"></a><dl>
<dt><b>RESOURCEDISPLAYTYPE_ROOT</b></dt>
<dt>0x00000007</dt>
</dl>
</td>
<td width="60%">
The object should be displayed as a logical root for the entire network.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCEDISPLAYTYPE_SHAREADMIN"></a><a id="resourcedisplaytype_shareadmin"></a><dl>
<dt><b>RESOURCEDISPLAYTYPE_SHAREADMIN</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The object should be displayed as a administrative share.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCEDISPLAYTYPE_DIRECTORY"></a><a id="resourcedisplaytype_directory"></a><dl>
<dt><b>RESOURCEDISPLAYTYPE_DIRECTORY</b></dt>
<dt>0x00000009</dt>
</dl>
</td>
<td width="60%">
The object should be displayed as a directory.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCEDISPLAYTYPE_TREE"></a><a id="resourcedisplaytype_tree"></a><dl>
<dt><b>RESOURCEDISPLAYTYPE_TREE</b></dt>
<dt>0x0000000A</dt>
</dl>
</td>
<td width="60%">
The object should be displayed as a tree. This display type was used for a NetWare Directory Service (NDS) tree by the NetWare Workstation service supported on Windows XP and earlier.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCEDISPLAYTYPE_NDSCONTAINER"></a><a id="resourcedisplaytype_ndscontainer"></a><dl>
<dt><b>RESOURCEDISPLAYTYPE_NDSCONTAINER</b></dt>
<dt>0x0000000A</dt>
</dl>
</td>
<td width="60%">
The object should be displayed as a Netware Directory Service container. This display type was used by the NetWare Workstation service supported on Windows XP and earlier.

</td>
</tr>
</table>
 


### -field dwUsage

Type: <b>DWORD</b>

A set of bit flags describing how the resource can be used. 




Note that this member can be specified only if the <b>dwScope</b> member is equal to <b>RESOURCE_GLOBALNET</b>. This member can be one of the following values defined in the <i>Winnetwk.h</i> header file. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RESOURCEUSAGE_CONNECTABLE"></a><a id="resourceusage_connectable"></a><dl>
<dt><b>RESOURCEUSAGE_CONNECTABLE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The resource is a connectable resource; the name pointed to by the <b>lpRemoteName</b> member can be passed to the 
<a href="https://msdn.microsoft.com/9f2cf166-eb08-4498-8cda-79808776a452">WNetAddConnection</a> function to make a network connection.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCEUSAGE_CONTAINER"></a><a id="resourceusage_container"></a><dl>
<dt><b>RESOURCEUSAGE_CONTAINER</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The resource is a container resource; the name pointed to by the <b>lpRemoteName</b> member can be passed to the 
<a href="https://msdn.microsoft.com/d99a549a-bf27-497f-a3be-bbe2c668bf90">WNetOpenEnum</a> function to enumerate the resources in the container.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCEUSAGE_NOLOCALDEVICE"></a><a id="resourceusage_nolocaldevice"></a><dl>
<dt><b>RESOURCEUSAGE_NOLOCALDEVICE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The resource is not a local device.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCEUSAGE_SIBLING"></a><a id="resourceusage_sibling"></a><dl>
<dt><b>RESOURCEUSAGE_SIBLING</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The resource is a sibling. This value is not used by Windows.

</td>
</tr>
<tr>
<td width="40%"><a id="RESOURCEUSAGE_ATTACHED"></a><a id="resourceusage_attached"></a><dl>
<dt><b>RESOURCEUSAGE_ATTACHED</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
The resource must be attached. This value specifies that a function to enumerate resource this should fail if
                                      the caller is not authenticated, even if 
                                      the network permits enumeration without 
                                      authentication.

</td>
</tr>
</table>
 


### -field lpLocalName

Type: <b>LPTSTR</b>

If the <b>dwScope</b> member is equal to <b>RESOURCE_CONNECTED</b> or <b>RESOURCE_REMEMBERED</b>, this member is a pointer to a <b>null</b>-terminated character string that specifies the name of a local device. This member is <b>NULL</b> if the connection does not use a device.


### -field lpRemoteName

Type: <b>LPTSTR</b>

If the entry is a network resource, this member is a pointer to a <b>null</b>-terminated character string that specifies the remote network name.

If the entry is a current or persistent connection, <b>lpRemoteName</b> member points to the network name associated with the name pointed to by the <b>lpLocalName</b> member.

The string can be <b>MAX_PATH</b> characters in length, and it must follow the network provider's naming conventions.


### -field lpComment

Type: <b>LPTSTR</b>

A pointer to a <b>NULL</b>-terminated  string that contains a comment supplied by the network provider.


### -field lpProvider

Type: <b>LPTSTR</b>

A pointer to a <b>NULL</b>-terminated  string that contains the name of the provider that owns the resource. This member can be <b>NULL</b> if the provider name is unknown. To retrieve the provider name, you can call the 
<a href="https://msdn.microsoft.com/c1369098-c574-4d5f-8051-ca5aa548e63f">WNetGetProviderName</a> function.


## -remarks



The <b>NETRESOURCE</b> structure is returned during an enumeration of network resources. 
The <b>NETRESOURCE</b> structure is also specified when making or querying a network connection with calls to various Windows Networking functions.

For Microsoft network providers, the <b>lpRemoteName</b> member can contain an IPv4 address in dotted-decimal notation. An example for a share might be the following:

<code>\\192.168.1.1\share
</code>

For Microsoft network providers on Windows Vista and later, the <b>lpRemoteName</b> member can contain an IPv6 address. However, the IPv6 literal format must be used so that the IPv6 address is parsed correctly. An IPv6 literal address is of the form:

ipv6-address with the ':' characters replaced by '-' characters followed by the ".ipv6-literal.net" string.

For example, for the following IPv6 address:

<code>2001:4898:9:3:c069:aa97:fe76:2449
</code>

an example for a share might be the following:

<code>\\2001-4898-9-3-c069-aa97-fe76-2449.ipv6-literal.net\share</code>

Other network providers may also support a <b>lpRemoteName</b> member that contains an IPv4 or IPv6 address, but this is up to specific network provider.

For more information about setting the values of the <b>dwType</b>, <b>lpLocalName</b>, <b>lpRemoteName</b>, and <b>lpProvider</b> members, see 
<a href="https://msdn.microsoft.com/3ec4a397-e0d4-419c-9e12-6d76a87b1ca0">MultinetGetConnectionPerformance</a>, 
<a href="https://msdn.microsoft.com/faec728c-f19e-418c-9bdb-cde93e7d98fb">WNetAddConnection2</a>, 
<a href="https://msdn.microsoft.com/169c7bb4-cb08-424c-af79-2133684a99db">WNetAddConnection3</a>, 
<a href="https://msdn.microsoft.com/19273874-adf1-4ffb-8b83-0eaa64e4622e">WNetGetResourceInformation</a>, 
<a href="https://msdn.microsoft.com/6ad5e2c0-d557-43cc-8ccf-a21160e262f8">WNetGetResourceParent</a>, and 
<a href="https://msdn.microsoft.com/80fa471d-074c-468f-b90f-1636081e1583">WNetUseConnection</a> functions.




## -see-also




<a href="https://msdn.microsoft.com/3ec4a397-e0d4-419c-9e12-6d76a87b1ca0">MultinetGetConnectionPerformance</a>



<a href="https://msdn.microsoft.com/faec728c-f19e-418c-9bdb-cde93e7d98fb">WNetAddConnection2</a>



<a href="https://msdn.microsoft.com/169c7bb4-cb08-424c-af79-2133684a99db">WNetAddConnection3</a>



<a href="https://msdn.microsoft.com/c68fd9de-9f24-41f0-8b59-2d083fec8abf">WNetCloseEnum</a>



<a href="https://msdn.microsoft.com/2c58c6d0-d5fe-447e-be39-df34072c160e">WNetEnumResource</a>



<a href="https://msdn.microsoft.com/c1369098-c574-4d5f-8051-ca5aa548e63f">WNetGetProviderName</a>



<a href="https://msdn.microsoft.com/19273874-adf1-4ffb-8b83-0eaa64e4622e">WNetGetResourceInformation</a>



<a href="https://msdn.microsoft.com/6ad5e2c0-d557-43cc-8ccf-a21160e262f8">WNetGetResourceParent</a>



<a href="https://msdn.microsoft.com/d99a549a-bf27-497f-a3be-bbe2c668bf90">WNetOpenEnum</a>



<a href="https://msdn.microsoft.com/80fa471d-074c-468f-b90f-1636081e1583">WNetUseConnection</a>



<a href="https://msdn.microsoft.com/7668ac55-7104-4ddb-88eb-920cfe4e36fd">Windows Networking (WNet) Overview</a>



<a href="https://msdn.microsoft.com/7969ccbb-d1ae-4a1f-8b9c-862cc6ddef1a">Windows Networking Structures</a>
 

 

