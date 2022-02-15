---
UID: NF:ondemandconnroutehelper.GetInterfaceContextTableForHostName
title: GetInterfaceContextTableForHostName function (ondemandconnroutehelper.h)
description: This function retrieves an interface context table for the given hostname and connection profile filter.
helpviewer_keywords: ["GetInterfaceContextTableForHostName","GetInterfaceContextTableForHostName function [Network Awareness]","nla.getinterfacecontexttableforhostname","ondemandconnroutehelper/GetInterfaceContextTableForHostName"]
old-location: nla\getinterfacecontexttableforhostname.htm
tech.root: nla
ms.assetid: BD687853-6242-4A72-BACE-13B681FD4674
ms.date: 12/05/2018
ms.keywords: GetInterfaceContextTableForHostName, GetInterfaceContextTableForHostName function [Network Awareness], nla.getinterfacecontexttableforhostname, ondemandconnroutehelper/GetInterfaceContextTableForHostName
req.header: ondemandconnroutehelper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: OnDemandConnRouteHelper.lib
req.dll: OnDemandConnRouteHelper.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetInterfaceContextTableForHostName
 - ondemandconnroutehelper/GetInterfaceContextTableForHostName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OnDemandConnRouteHelper.dll
 - API-Ms-Win-Networking-InterfaceContexts-L1-1-0.dll
api_name:
 - GetInterfaceContextTableForHostName
---

# GetInterfaceContextTableForHostName function


## -description

This function retrieves an interface context table for the given hostname and connection profile filter.

## -parameters

### -param HostName [in, optional]

The destination hostname.

### -param ProxyName [in, optional]

The HTTP proxy name.

### -param Flags [in]

You can use the following flags.

<table></table>
 

<table>
<tr>
<td><b>Flag</b></td>
<td><b>Description</b></td>
</tr>
<tr>
<td><b>NET_INTERFACE_FLAG_NONE</b></td>
<td>Use the default behavior.</td>
</tr>
<tr>
<td><b>NET_INTERFACE_FLAG_CONNECT_IF_NEEDED</b></td>
<td>Indicates whether the underlying connection should be activated or not.</td>
</tr>
</table>

### -param ConnectionProfileFilterRawData [in, optional]

The connection profile filter blog which is a byte cast of wcm_selection_filters.

### -param ConnectionProfileFilterRawDataSize [in]

The size of the <i>ConnectionProfileFilterRawData</i> in bytes.

### -param InterfaceContextTable [out]

This is set to the list of <a href="/windows/win32/api/ondemandconnroutehelper/ns-ondemandconnroutehelper-net_interface_context">NET_INTERFACE_CONTEXT</a> structures containing the interface indices and configuration names that can be used for the hostname and filter.

## -returns

This function returns the following <b>HRESULT</b> values depending on the status.

<table></table>
 

<table>
<tr>
<td><b>HRESULT</b></td>
<td><b>Description</b></td>
</tr>
<tr>
<td><b>S_OK</b></td>
<td>
This is returned if a connection that satisfies the parameters and internal policies exists. <a href="/windows/win32/api/ondemandconnroutehelper/ns-ondemandconnroutehelper-net_interface_context">NET_INTERFACE_CONTEXT_TABLE</a> will contain a list of interfaces indices and configuration names of those connections. When S_OK is returned, <a href="/windows/desktop/api/ondemandconnroutehelper/nf-ondemandconnroutehelper-freeinterfacecontexttable">FreeInterfaceContextTable</a> should be called to release the context table.

</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>
This is returned to indicate that any connection or default interface can be used for this hostname and filter. The <a href="/windows/win32/api/ondemandconnroutehelper/ns-ondemandconnroutehelper-net_interface_context">NET_INTERFACE_CONTEXT_TABLE</a> will be null in this case because the caller can use the default route to satisfy the requirements.

</td>
</tr>
<tr>
<td><b>E_NOTFOUND</b></td>
<td>
This is returned if no connection is currently available or existing connection don't meet the connection filter and the internal policy for the host. The exact return code would be <b>HRESULT(ERROR_NOT_FOUND)</b>

</td>
</tr>
<tr>
<td><b>E_INVALIDARG</b></td>
<td>
This is returned if the caller passes an invalid argument, uses an unsupported flag, has a bad connection filter data, incorrect size or null <a href="/windows/win32/api/ondemandconnroutehelper/ns-ondemandconnroutehelper-net_interface_context">NET_INTERFACE_CONTEXT_TABLE</a>


</td>
</tr>
<tr>
<td><b>E_OUTOFMEMORY</b></td>
<td>
This is returned if there is not enough memory to complete the operation.

</td>
</tr>
<tr>
<td><b>FAILED(HRESULT)</b></td>
<td>
This is returned because of failures that are outside the control of this function.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ondemandconnroutehelper/nf-ondemandconnroutehelper-freeinterfacecontexttable">FreeInterfaceContextTable</a>



<a href="/windows/win32/api/ondemandconnroutehelper/ns-ondemandconnroutehelper-net_interface_context">NET_INTERFACE_CONTEXT_TABLE</a>