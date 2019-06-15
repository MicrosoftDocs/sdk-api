---
UID: NF:npapi.NPGetCaps
title: NPGetCaps function (npapi.h)
author: windows-sdk-content
description: Returns information about which services are supported on the network.
old-location: security\npgetcaps.htm
tech.root: SecAuthN
ms.assetid: 8d399bae-4084-4f06-b7f5-036a54d8d90e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: NPGetCaps, NPGetCaps function [Security], WNNC_ADMIN, WNNC_CONNECTION, WNNC_DIALOG, WNNC_ENUMERATION, WNNC_NET_TYPE, WNNC_SPEC_VERSION, WNNC_START, WNNC_USER, _mnp_npgetcaps, npapi/NPGetCaps, security.npgetcaps
ms.topic: function
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Npapi.h
api_name:
 - NPGetCaps
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# NPGetCaps function


## -description


Returns information about which services are supported on the network.


## -parameters




### -param ndex [in]

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
The <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">state</a> of the network provider.

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




## -remarks



When a start time is returned by <b>NPGetCaps</b>, the MPR uses this value to determine when to try to start all network providers again. MPR uses the longest start time returned by the providers it called.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/npapi/nf-npapi-nplogonnotify">NPLogonNotify</a>



<a href="https://docs.microsoft.com/windows/desktop/api/npapi/nf-npapi-nppasswordchangenotify">NPPasswordChangeNotify</a>
 

 

