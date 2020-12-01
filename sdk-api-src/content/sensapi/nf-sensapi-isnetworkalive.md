---
UID: NF:sensapi.IsNetworkAlive
title: IsNetworkAlive function (sensapi.h)
description: The IsNetworkAlive function determines whether or not a local system is connected to a network, and identifies the type of network connection, for example, a LAN, WAN, or both.
helpviewer_keywords: ["IsNetworkAlive","IsNetworkAlive function [SENS]","_zaw_isnetworkalive","sens.isnetworkalive","sensapi/IsNetworkAlive","syncmgr.isnetworkalive"]
old-location: sens\isnetworkalive.htm
tech.root: Sens
ms.assetid: 1a2f3acd-0626-4fb2-8c5f-f3a0704cc0b4
ms.date: 12/05/2018
ms.keywords: IsNetworkAlive, IsNetworkAlive function [SENS], _zaw_isnetworkalive, sens.isnetworkalive, sensapi/IsNetworkAlive, syncmgr.isnetworkalive
req.header: sensapi.h
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
req.lib: Sensapi.lib
req.dll: Sensapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IsNetworkAlive
 - sensapi/IsNetworkAlive
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Sensapi.dll
api_name:
 - IsNetworkAlive
---

# IsNetworkAlive function


## -description

The 
<b>IsNetworkAlive</b> function determines whether or not a   local system is connected to a network, and identifies the type of network connection, for example, a LAN, WAN, or both.

## -parameters

### -param lpdwFlags [out]

The type of network connection that is available. This parameter can be one of the following values: 







#### NETWORK_ALIVE_LAN

The computer has one or more LAN cards that are active.



#### NETWORK_ALIVE_WAN

The computer has one or more active RAS connections.

## -returns

Always call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> before checking the return code of this function.  If the last error is not 0, the <b>IsNetworkAlive</b> function has failed and the following <b>TRUE</b> and <b>FALSE</b> values do not apply.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
If the last error is 0 and the function returns <b>TRUE</b>, SENS has determined that a  local system is connected to a network. 

For information about the type of connection, see the <i>lpdwFlags</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
If the last error is 0 and the function returns <b>FALSE</b>, SENS has determined there is no connection. 

</td>
</tr>
</table>

## -remarks

Starting with applications designed for Windows Vista and Windows Server 2008, developers should consider using the <a href="/windows/desktop/NLA/portal">Network List Manager</a> instead of this function.

This function can be used by an application to determine whether or not there is network connectivity before proceeding with network operations. A directory service type of application, e-mail client, or Internet browser can adapt to various types of network connectivity. For example, a printing operation can be deferred until a network connection is available.

It may not always be practical for an application to call 
<b>IsNetworkAlive</b> to determine whether or not a  local system is disconnected from a LAN, because <b>IsNetworkAlive</b> can be slow, and it may take too much time for the function to detect that a local system is disconnected. 
However, <b>IsNetworkAlive</b> can always identify a WAN connectivity at the moment.

<div class="alert"><b>Note</b>  This function is only available for TCP/IP connections.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Sens/about-system-event-notification-service">About System Event Notification Service</a>



<a href="/windows/desktop/api/sensapi/nf-sensapi-isdestinationreachablea">IsDestinationReachable</a>