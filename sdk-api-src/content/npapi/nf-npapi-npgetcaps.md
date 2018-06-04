---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# NPGetCaps function


## -description


Returns information about which services are supported on the network.


## -parameters




### -param ndex

TBD




#### - nIndex [in]

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
The <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">state</a> of the network provider.

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




<a href="https://msdn.microsoft.com/9b0e5646-ac57-4eae-bad7-a16c07b51f4b">NPLogonNotify</a>



<a href="https://msdn.microsoft.com/5c7f5672-f379-4518-ae60-4f7d7e4caffa">NPPasswordChangeNotify</a>
 

 

