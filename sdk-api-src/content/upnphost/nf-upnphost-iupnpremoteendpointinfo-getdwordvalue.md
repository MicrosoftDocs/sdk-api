---
UID: NF:upnphost.IUPnPRemoteEndpointInfo.GetDwordValue
title: IUPnPRemoteEndpointInfo::GetDwordValue
author: windows-sdk-content
description: The GetDwordValue method gets a 4-byte value that provides information about either a request or requester.
old-location: upnp\iupnpremoteendpointinfo_getdwordvalue.htm
old-project: UPnP
ms.assetid: efbb0671-cb32-41e1-8405-1d145c247673
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: AF_INET, AF_INET6, GetDwordValue, GetDwordValue method [UPnP APIs], GetDwordValue method [UPnP APIs],IUPnPRemoteEndpointInfo interface, IUPnPRemoteEndpointInfo interface [UPnP APIs],GetDwordValue method, IUPnPRemoteEndpointInfo.GetDwordValue, IUPnPRemoteEndpointInfo::GetDwordValue, upnp.iupnpremoteendpointinfo_getdwordvalue, upnphost/IUPnPRemoteEndpointInfo::GetDwordValue
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: upnphost.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: UI_EVENTPARAMS_COMMAND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnphost.dll
api_name:
 - IUPnPRemoteEndpointInfo.GetDwordValue
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnphost.dll
req.irql: 
req.product: Windows UI
---

# IUPnPRemoteEndpointInfo::GetDwordValue


## -description


The <b>GetDwordValue</b> method gets a 4-byte value that provides information about either a request or requester.


## -parameters




### -param bstrValueName [in]

String that specifies the category of information to be retrieved.


### -param pdwValue [out]

Pointer to a 4-byte value, the meaning of which depends on the value of <i>bstrValueName</i>.

If <i>bstrValueName</i> is "AddressFamily", the 4-byte value indicates the format of the requester's IP address as follows. The values are defined in Winsock2.h.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AF_INET"></a><a id="af_inet"></a><dl>
<dt><b>AF_INET</b></dt>
</dl>
</td>
<td width="60%">
IP (IP version 4)

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET6"></a><a id="af_inet6"></a><dl>
<dt><b>AF_INET6</b></dt>
</dl>
</td>
<td width="60%">
IP6 (IP version 6)

</td>
</tr>
</table>
 


## -returns



If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -remarks



Currently, the only valid value for the <i>bstrValueName</i> parameter is "AddressFamily". For any other value, this method will return the COM error code E_INVALIDARG.




## -see-also




<a href="https://msdn.microsoft.com/4cbfaa8c-80f1-49c6-91aa-17764559da8b">GetGuidValue</a>



<a href="https://msdn.microsoft.com/c3b0dcd2-2195-4e09-aac4-073a3d848fa9">GetStringValue</a>



<a href="https://msdn.microsoft.com/32e246cd-50eb-4221-8166-a7cd8ed42d69">IUPnPRemoteEndpointInfo</a>
 

 

