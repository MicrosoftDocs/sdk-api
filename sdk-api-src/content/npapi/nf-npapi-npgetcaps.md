---
UID: NF:npapi.NPGetCaps
title: NPGetCaps function (npapi.h)
description: Returns information about which services are supported on the network.
helpviewer_keywords: ["NPGetCaps","NPGetCaps function [Security]","WNNC_ADMIN","WNNC_CONNECTION","WNNC_DIALOG","WNNC_ENUMERATION","WNNC_NET_TYPE","WNNC_SPEC_VERSION","WNNC_START","WNNC_USER","_mnp_npgetcaps","npapi/NPGetCaps","security.npgetcaps"]
old-location: security\npgetcaps.htm
tech.root: security
ms.assetid: 8d399bae-4084-4f06-b7f5-036a54d8d90e
ms.date: 12/05/2018
ms.keywords: NPGetCaps, NPGetCaps function [Security], WNNC_ADMIN, WNNC_CONNECTION, WNNC_DIALOG, WNNC_ENUMERATION, WNNC_NET_TYPE, WNNC_SPEC_VERSION, WNNC_START, WNNC_USER, _mnp_npgetcaps, npapi/NPGetCaps, security.npgetcaps
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
 - NPGetCaps
 - npapi/NPGetCaps
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
 - NPGetCaps
---

# NPGetCaps function


## -description

Returns information about which services are supported on the network.

## -parameters

### -param nIndex [in]

Specifies the type of information to return. The following values are defined. 




               

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WNNC_ADMIN"></a><a id="wnnc_admin"></a><dl>
<dt><b>WNNC_ADMIN</b></dt>
</dl>
</td>
<td width="60%">
A bitmask that indicates which administrative functions the network provider supports.

</td>
</tr>
<tr>
<td width="40%"><a id="WNNC_CONNECTION"></a><a id="wnnc_connection"></a><dl>
<dt><b>WNNC_CONNECTION</b></dt>
</dl>
</td>
<td width="60%">
A bitmask that indicates which connection functions the network provider supports.

</td>
</tr>
<tr>
<td width="40%"><a id="WNNC_DIALOG"></a><a id="wnnc_dialog"></a><dl>
<dt><b>WNNC_DIALOG</b></dt>
</dl>
</td>
<td width="60%">
A bitmask that indicates which provider-specific dialog box functions the network provider supports.

</td>
</tr>
<tr>
<td width="40%"><a id="WNNC_ENUMERATION"></a><a id="wnnc_enumeration"></a><dl>
<dt><b>WNNC_ENUMERATION</b></dt>
</dl>
</td>
<td width="60%">
A bitmask that indicates which enumeration functions the network provider supports.

</td>
</tr>
<tr>
<td width="40%"><a id="WNNC_NET_TYPE"></a><a id="wnnc_net_type"></a><dl>
<dt><b>WNNC_NET_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Network type and provider version.

</td>
</tr>
<tr>
<td width="40%"><a id="WNNC_SPEC_VERSION"></a><a id="wnnc_spec_version"></a><dl>
<dt><b>WNNC_SPEC_VERSION</b></dt>
</dl>
</td>
<td width="60%">
WNet API version supported by the provider.

</td>
</tr>
<tr>
<td width="40%"><a id="WNNC_START"></a><a id="wnnc_start"></a><dl>
<dt><b>WNNC_START</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/SecGloss/s-gly">state</a> of the network provider.

</td>
</tr>
<tr>
<td width="40%"><a id="WNNC_USER"></a><a id="wnnc_user"></a><dl>
<dt><b>WNNC_USER</b></dt>
</dl>
</td>
<td width="60%">
A bitmask that indicates which user functions the network provider supports.

</td>
</tr>
</table>

## -returns

The <b>NPGetCaps</b> function returns either a constant or a bitmask, depending on the value of the <i>nIndex</i> parameter. A few of the <i>nIndex</i> values cause a constant to be returned. But in most cases, the <i>nIndex</i> parameter specifies which set of services to query, and the returned value is a bitmask that indicates which services in this set are supported. In these cases, a zero return value indicates that none of the services in the set are supported.

The following list shows the values that <i>nIndex</i> may contain, each followed by a description of what is returned for that value.

####WNNC_ADMIN
Returns a mask that indicates which of the administrative functions the network provider supports. This can be one or more of the following.

| Flag |	Function supported |
| -----|------------------------ |
WNNC_ADM_DIRECTORYNOTIFY | [NPDirectoryNotify](./nf-npapi-npdirectorynotify.md)
WNNC_ADM_GETDIRECTORYTYPE | [NPGetDirectoryType](./nf-npapi-npgetdirectorytype.md)

 

####WNNC_CONNECTION
Returns a mask that indicates which of the connection functions the network provider supports. This can be one or more of the following.

| Flag |	Function supported |
| -----|------------------------ |
| WNNC_CON_ADDCONECTION (0x00000001) | [NPAddConnection](./nf-npapi-npaddconnection.md) | 
| WNNC_CON_CANCELCONNECTION (0x00000002) | [NPCancelConnection](./nf-npapi-npcancelconnection.md) |
| WNNC_CON_GETCONNECTIONS (0x00000004) | [NPGetConnection](./nf-npapi-npgetconnection.md) |
| WNNC_CON_ADDCONECTION3 (0x00000008) | [NPAddConnection3](./nf-npapi-npaddconnection3.md) |
| WNNC_CON_GETPERFORMANCE (0x00000040) | [NPGetConnectionPerformance](./nf-npapi-npgetconnectionperformance.md) |
| WNNC_CON_DEFER (0x00000080) | Deferred connections are supported with [NPAddConnection3](./nf-npapi-npaddconnection3.md). |


####WNNC_DIALOG
Returns a mask that indicates which of the dialog box functions the network provider supports. This can be one or more of the following.

| Flag |	Function supported |
| -----|------------------------ |
| WNNC_DLG_DEVICEMODE| [NPDeviceMode](./nf-npapi-npdevicemode.md) |
| WNNC_DLG_FORMATNETNAME| [NPFormatNetworkName](./nf-npapi-npformatnetworkname.md) |
| WNNC_DLG_GETRESOURCEINFORMATION | [NPGetResourceInformation](./nf-npapi-npgetresourceinformation.md) |
| WNNC_DLG_GETRESOURCEPARENT | [NPGetResourceParent](./nf-npapi-npgetresourceparent.md) |
| WNNC_DLG_PERMISSIONEDITOR | This flag is not used. |
| WNNC_DLG_PROPERTYDIALOG | [NPPropertyDialog](./nf-npapi-nppropertydialog.md) and NPGetPropertyText |
| WNNC_DLG_SEARCHDIALOG | [NPSearchDialog](./nf-npapi-npsearchdialog.md) |

 

####WNNC_ENUMERATION

Returns a mask that indicates which scopes of enumeration, if any, are supported. For more information about enumeration scopes, see the Parameters section in the reference topic NPOpenEnum. This can be one or more of the following.

| Flag | Enumeration type supported |
-------|-----------------------------
| WNNC_ENUM_GLOBAL (0x00000001) | [NPOpenEnum](./nf-npapi-npopenenum.md) is implemented and supports a scope of all resources on the network. In other words, NPOpenEnum supports RESOURCE_GLOBALNET. |
| WNNC_ENUM_LOCAL (0x00000002) | [NPOpenEnum](./nf-npapi-npopenenum.md) is implemented and supports a scope of all currently connected resources. In other words, NPOpenEnum supports RESOURCE_CONNECTED.|
| WNNC_ENUM_CONTEXT (0x00000004) | [NPOpenEnum](./nf-npapi-npopenenum.md) is implemented and supports a scope of all resources associated with the user's current and default network context. In other words, NPOpenEnum supports RESOURCE_CONTEXT. |

**Note** If WNNC_ENUMERATION returns a nonzero bitmask, you know that the network provider supports [NPOpenEnum](./nf-npapi-npopenenum.md) and can infer that the provider also supports [NPEnumResource](./nf-npapi-npenumresource.md) and [NPCloseEnum](./nf-npapi-npcloseenum.md). This is because a network provider that supports NPOpenEnum is also expected to support NPEnumResource and NPCloseEnum.
 
####WNNC_NET_TYPE
Returns a value that indicates the type of network that the network provider supports. The high word contains the provider type, and the low word may contain a subtype. Developers who are working on new providers should obtain a new network type from Microsoft. A provider that does not return the correct network type may cause the WNET functions to behave in unpredictable ways.

The network type can be one of the following.

* WNNC_NET_10NET
* WNNC_NET_INTERGRAPH
* WNNC_NET_3IN1
* WNNC_NET_LANMAN
* WNNC_NET_9TILES
* WNNC_NET_LANSTEP
* WNNC_NET_APPLETALK
* WNNC_NET_LANTASTIC
* WNNC_NET_AS400
* WNNC_NET_LIFENET
* WNNC_NET_BMC
* WNNC_NET_LOCUS
* WNNC_NET_BWNFS
* WNNC_NET_MASFAX
* WNNC_NET_CLEARCASE
* WNNC_NET_MSNET
* WNNC_NET_COGENT
* WNNC_NET_NETWARE
* WNNC_NET_CSC
* WNNC_NET_OBJECT_DIRE
* WNNC_NET_DCE
* WNNC_NET_PATHWORKS
* WNNC_NET_DECOREB
* WNNC_NET_POWERLAN
* WNNC_NET_DISTENCT
* WNNC_NET_PROTSTOR
* WNNC_NET_EXTENDNET
* WNNC_NET_RDR2SAMPLE
* WNNC_NET_FARALLON
* WNNC_NET_SHIVA
* WNNC_NET_FJ REDIR
* WNNC_NET_SUN_PC_NFS
* WNNC_NET_FRONTIER
* WNNC_NET_SYMFONET
* WNNC_NET_FTP_NFS
* WNNC_NET_TWINS
* WNNC_NET_HOB_NFS
* WNNC_NET_VINES
* WNNC_NET_IBMAL
 

####WNNC_SPEC_VERSION
Returns WNNC_SPEC_VERSION51. The high and low words of the return value contain the major and minor version numbers of the WNet API specification supported by the credential manager.

####WNNC_START
Returns one of the following values to indicate if and when the provider is likely to start. The MPR will wait for the longest time-out period specified by all network providers.

| Flag| Start time |
|-----|-----|
| 0x0 | Indicates the provider will not start, for example, if it is disabled. The MPR will not retry starting the network provider. |
| Time | Indicates the time, in milliseconds, until the provider starts. |
| 0xFFFFFFFF | Indicates that the provider does not know when it will start. If the network provider returns this value, the MPR uses its default value, 60 seconds.|
| 0x1 | Indicates that the provider is already started. |

 
####WNNC_USER
Returns WNNC_USR_GETUSER if the network provider supports the [NPGetUser](./nf-npapi-npgetuser.md) function.

## -remarks

When a start time is returned by <b>NPGetCaps</b>, the MPR uses this value to determine when to try to start all network providers again. MPR uses the longest start time returned by the providers it called.

## -see-also

<a href="/windows/desktop/api/npapi/nf-npapi-nplogonnotify">NPLogonNotify</a>



<a href="/windows/desktop/api/npapi/nf-npapi-nppasswordchangenotify">NPPasswordChangeNotify</a>